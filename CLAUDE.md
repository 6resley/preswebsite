# preswebsite

Presley Jackson's portfolio site: a single self-contained `index.html` (images embedded as base64 WebP), hosted on GitHub Pages from `main` at www.presjackson.com (DNS on Cloudflare, records set to DNS only).

## Workflow
- The owner has given standing permission to merge pull requests into `main` without asking. After verifying a change in a browser, open the PR and merge it right away, then tell the owner it's live.
- Keep `CNAME` (`www.presjackson.com`) and `.nojekyll` in the repo root; GitHub Pages needs them.

## Page structure notes
- Projects live in `DEFAULT_IMAGES` (keyed by project slug) and in the `.work-row` elements inside `#workList`. The rows are hidden but still drive the project popup, the "Next project" button, the hero tunnel cards and the glass folders (`#folderGrid`), so edit project names/tags/years there.
- Folder labels come from `NAMES` in the glass-folder script; no second line (owner removed counts). No dates anywhere (owner's call: the work spans years).
- `photography` is an empty project ("Coming soon" folder that can't open). Add images to `DEFAULT_IMAGES['photography']` (WebP data URIs, ~1400px, like the others) and it becomes a normal folder automatically.
