# Kong Fam — VivoCity Dining Codex

A single-page dining directory for the 77 food outlets at VivoCity,
1 HarbourFront Walk, Singapore 098585.

**Features**
- Filter by cuisine (12 categories), search, and six sort orders
- Google rating and review count shown on each card
- Indicative per-pax price estimate
- One-tap `tel:` reservation link (63 of 77 outlets have a direct line)
- "I dined in" visit log with running stats, saved in the browser
- Randomiser with eight picking rules for when nobody can decide

## Deploy to Vercel via GitHub

1. Create a new **empty** repository on GitHub (private is fine).
2. Upload the contents of this folder to the repo root — `index.html`
   must sit at the top level, not inside a subfolder.
3. Go to vercel.com, choose **Add New → Project**, and import the repo.
4. Framework Preset: **Other**. Leave Build Command and Output Directory
   blank — this is a static site with no build step.
5. Click **Deploy**. It goes live in under a minute.

Any push to the default branch redeploys automatically.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The entire site — HTML, CSS and JS in one file, no dependencies |
| `vercel.json` | Clean URLs and basic security headers |
| `.gitignore` | Keeps OS junk and `.vercel` out of the repo |

## Notes

- **Where the visit log lives.** Entries are saved to the browser's own
  storage on the device that logged them. They are not synced between
  phones and are lost if that browser's site data is cleared. Use
  *Copy log as text* to keep a backup.
- **The data is a snapshot.** Ratings, review counts, unit numbers and
  phone lines came from Google Places on 17 August 2026 and will drift.
  To refresh, edit the `const R = [...]` array near the top of the
  `<script>` block in `index.html`.
- **Per-pax figures are estimates**, not quoted prices. They exclude
  drinks, GST and service charge.
- **Keep it unlisted.** The page carries a `noindex` tag. Marvel
  character names are used as nicknames for private family use only —
  do not attach this to a business, run ads against it, or promote it
  publicly.
