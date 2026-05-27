# Defence & Athletics — Client Progress CRM

A single-file web app for tracking client plans, levels, and striking-skill progress.
No build tools, no server, no dependencies to install. It's one HTML file.

---

## What it does

- **Dashboard** — active clients, sessions remaining, average skill mastery, and a "plans running low" alert.
- **Clients roster** — searchable, filterable by level, with plan-usage and mastery bars.
- **Client profile** — contact details, level (Beginner / Intermediate / Advanced), plan usage with one-tap session logging, ten striking skill areas rated 0–5, coach notes, and a dated progress log.

Data saves automatically to the browser using `localStorage`.

---

## Put it live on GitHub Pages (free)

1. **Create a GitHub account** at https://github.com if you don't have one.
2. **Create a new repository**: click **+** (top right) → *New repository*.
   - Name it e.g. `da-crm`
   - Set it to **Public**
   - Tick *Add a README* (optional)
   - Click *Create repository*
3. **Upload the app**: in the repo click *Add file → Upload files*, drag in `index.html`, then *Commit changes*.
4. **Turn on Pages**: go to *Settings → Pages*. Under "Branch" choose `main` and `/ (root)`, then *Save*.
5. **Wait about a minute**, refresh the Pages settings screen, and your live URL appears at the top
   (it looks like `https://YOUR-USERNAME.github.io/da-crm/`).

Open that link on any phone, tablet, or laptop. To bookmark it on a tablet for front-desk use,
open it in the browser and "Add to Home Screen".

### Updating it later
Re-upload a new `index.html` (Upload files → commit). Pages redeploys automatically within a minute.

---

## Important things to know

- **Data lives on the device/browser that opens the app.** Two coaches on two different tablets
  keep two separate rosters — they do **not** sync. For a single shared front-desk tablet this is fine.
  Multi-coach shared data needs a backend/database, which is a larger separate project.
- **Don't clear browser data** for the site, or the saved roster on that device is wiped.
  Consider periodically writing key info down elsewhere as backup until an export feature is added.
- **Needs internet** the first time it loads (it pulls React and fonts from a CDN).
  After that most browsers cache it, but a connection is recommended.

---

## Editing the app

Everything is inside `index.html`. To change the skill list, find the `SKILL_AREAS` array near the top
and add/rename items. To change plan types, edit `PLAN_TYPES`. The starter clients are in the `SEED` array
(delete them in-app once you've added real ones).
