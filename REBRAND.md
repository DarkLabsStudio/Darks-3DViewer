# Rebranding status: Online 3D Viewer → Darks 3DViewer

This repository is a fork of [Online 3D Viewer](https://github.com/kovacsv/Online3DViewer).
This document tracks the rebranding work so it is clear what has changed and what is still open.

## Done

* **Product name** - every user-facing occurrence of the original name is now **Darks 3DViewer**:
  website titles, intro and dialog strings, manual, FAQ, cookie policy, sandbox pages, generated documentation and README.
* **Package metadata** - `name` is `darks-3dviewer`, `description` is `Darks 3DViewer`,
  `repository` points to `github.com/DarkLabsStudio/Darks-3DViewer` (package.json and package-lock.json).
* **Project links** - GitHub links (repository, issues, releases) and the developer documentation link
  now point to the DarkLabsStudio repository.
* **Docs** - `docs/source` templates and the generated pages in `docs/` use the new name and repository.
* **Logo asset names** - served assets renamed from `3dviewer_net_*` to `darks_3dviewer_*`
  (favicon, mark, wordmark, social image, docs favicon), with all references updated.
* **Wordmark** - `darks_3dviewer_logo_text.svg` is a new lockup: the original cube mark followed by
  "DARKS 3DVIEWER". It scales to the existing 190x40 header and 381x80 intro slots and follows the
  `--ov_logo_text_color` theme variable in light and dark mode.
* **Legal** - `LICENSE.md` keeps the original MIT copyright and adds the fork's copyright line.
  A Credits section in the README attributes the upstream project.
* **Issue templates** - reworded for the Darks 3DViewer website.

## Deliberately unchanged (compatibility / pending decisions)

* **Domain** - `https://3dviewer.net` is still used for canonical URLs, share links, embed snippets,
  the `.htaccess` redirect and exported file metadata. These are centralized enough to swap later:
  `source/website/sharingdialog.js`, `source/engine/export/exportergltf.js`,
  `source/engine/export/exporterobj.js`, `website/index.html`, `website/info/index.html`,
  `website/.htaccess` and `test/tests/exporter_test.js` (keep the last one in sync).
* **Engine artifact names** - `o3dv.min.js`, `o3dv.module.js`, `o3dv.website.min.js`, the `OV` global and
  the `ov_` CSS prefix are the public build/API surface and were not renamed.
* **Embed class name** - `online_3d_viewer` stays, so existing embedded viewers keep working.
* **Upstream reference** - the comment in `source/engine/threejs/threeutils.js` still links to the
  upstream issue it documents.
* **Funding** - `.github/FUNDING.yml` still points to the upstream sponsorship accounts.

## Open items

1. **Domain** - register a domain and replace `3dviewer.net` everywhere listed above (including `.htaccess`).
2. **Logo art** - the cube mark is unchanged and the social share image
   (`darks_3dviewer_logo_social.png`) still shows the old branding. The legacy masters live in
   `assets/logos/upstream/`; a proper brand pass should replace the 512px icon, social image and favicon.
3. **npm package** - `darks-3dviewer` is not published yet; publish it before the Installation guide links
   are valid. Consider a fork-specific version, e.g. `0.19.0-darks.1`.
4. **Docs** - run `npm run generate_docs` after `npm install` to confirm the generator output matches the
   edited pages in `docs/`.
5. **Community** - the README no longer links the upstream Discord invite; add an official support channel
   when one exists.
