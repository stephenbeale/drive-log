# Drive Log

A journey timer for leisure driving: times drives, logs slow points, records the route, tracks fuel and estimates fuel cost.

## Files

- `drive-log.artifact.html` is the only source file. It runs as a Claude artifact and as the GitHub Pages site.
- `index.html` is generated from it by `./build.sh`. Never edit it by hand. Run `./build.sh` after every change to the source.
- Pushing to `main` deploys GitHub Pages automatically (about a minute).

## Two versions

| | GitHub Pages | Claude artifact |
|---|---|---|
| URL | https://stephenbeale.github.io/drive-log/ | https://claude.ai/artifact/TTxZeWCY845egzStUz1kKZ |
| Location / GPS | Yes | No, blocked by the viewer |
| Photo reading | Tesseract on the phone | Claude (`sample` capability) |
| Place names | postcodes.io | Claude |
| Data | Browser `localStorage` on that device | User's Claude account (`db`, private per user) |

When changing the page, update both: push to GitHub and republish the artifact from the same source file.

## Working with the user

- **Every time the user asks where or how to test, and after every change you ship**, end your reply with a table of test links:
  - Columns: link, what it is, best for, notes.
  - Include the GitHub Pages site, the Claude artifact and the repo.
  - Below the table, say which commit is live and whether the Pages deploy succeeded. Check the "pages build and deployment" workflow run.
  - Add a short "what to test" list covering the latest changes.
  - Add anything else needed to test, such as first-time setup or a cache refresh.
- Never suggest touching the phone while driving. Hands-free features must work without input; manual controls are labelled for passengers or when parked.
- UK conventions: miles, UK MPG (4.54609 L per gallon), pence per litre, £.
