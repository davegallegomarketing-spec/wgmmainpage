# Discovering Your Values — Workbook (web version)

A single-page, fillable web version of the Wing Girl Method "Discovering Your Values
and Owning Them" workbook. Built to match the approved PDF branding.

## What it does
- All 18 questions plus the pages 8–11 guidance from the PDF
- Auto-saves as you type, on the user's own device (browser `localStorage`)
- Close the tab and come back — answers are still there
- "Download as PDF" produces a clean printable copy with answers as flowing text
- Nothing is sent to any server. No data is collected.

## Files
- `index.html` — the workbook (this is the whole app)
- `robots.txt` — tells search engines not to crawl it
- `vercel.json` — adds a `noindex` HTTP header (second layer of search-engine blocking)

## Put it on GitHub
1. Create a new repository (keep it Private while testing).
2. Add these three files to the root of the repo. `index.html` must keep that
   exact name so the site loads at the root URL.
3. Commit and push.

## Deploy to Vercel
1. vercel.com → Add New → Project → Import this repository.
2. Framework preset: **Other**. No build command, no output directory — it's static.
3. Deploy. You'll get a URL like `your-project.vercel.app`.

## Test saving the right way
Open the **real deployed URL** directly (not the preview-inside-a-frame view).
Type an answer, refresh the page — it should still be there.

## Keep it private while testing
In the Vercel project: Settings → Deployment Protection → turn on protection so
only you (logged into Vercel) can open it. `noindex` keeps it out of Google, but
anyone with the link can still open it unless Deployment Protection is on.

## Important note on saving
Answers save per-device, per-browser — same as the current PDF. They do NOT sync
across phones/computers and are NOT visible to anyone else. Cross-device accounts
would require a server and database, which changes the privacy and legal picture.
