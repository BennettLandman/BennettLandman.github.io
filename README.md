# bennettlandman.github.io

The GitHub **user site** for this account — everything in this repo is served
from the root of `https://bennettlandman.github.io/`.

## Why this repo exists

Google's OAuth consent screen requires the app home page to be on a domain
whose ownership you can prove in Google Search Console. A GitHub *project*
page (like `bennettlandman.github.io/pawgress-kmp/`) only lets you control a
path, not the root of the subdomain — so Search Console can't verify the
subdomain itself, and Google rejects the home page with "the website of your
home page URL is not registered to you."

A **user site** repo serves the root of that subdomain, which makes
verification possible: drop Search Console's verification file in this folder,
or paste its meta tag into `index.html`, and the whole `bennettlandman.github.io`
subdomain — including `/pawgress-kmp/` — is verified.

## ⚠️ This repo must be named `BennettLandman.github.io`

GitHub only treats a repo as a **user site** (served at the domain root) when
its name is exactly `<username>.github.io`. A repo named just `bennettlandman`
is something else entirely — GitHub's *profile README* repo — and its Pages
would be served at `bennettlandman.github.io/bennettlandman/`, a project page
at a sub-path, which does not solve the verification problem at all.

If this repo is still named `bennettlandman` on GitHub, rename it:
**Settings → General → Repository name →** `BennettLandman.github.io` → Rename.
Renaming keeps the history and sets up redirects from the old name, so the
existing `origin` remote keeps working.

The local folder name doesn't matter — only the name on GitHub does.

## Setup

1. Rename the repo on GitHub as above (if not already done).
2. Push this folder.
3. Confirm GitHub Pages is on: Settings → Pages. User sites normally enable
   themselves; if not, set the source to the `main` branch, root folder.
4. In [Google Search Console](https://search.google.com/search-console), add a
   **URL prefix** property for `https://bennettlandman.github.io/`, pick a
   verification method, and put the file or meta tag here (see the comment at
   the top of `index.html`).

A URL-prefix property verified at the root covers every path beneath it, so the
Pawgress pages living in the `pawgress-kmp` repo stay exactly where they are.
