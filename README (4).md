# EngInQuire

> First-year engineering, decoded. Pre-semester review sessions and free study resources for incoming Schulich engineering students at the University of Calgary.

Built and run by **Jacob Hailemariam** and **Tom Kurian**.

**Live site:** `https://YOUR-USERNAME.github.io/enginquire/`
*(replace with the real URL once GitHub Pages is on — see below)*

**Contact:** enginquire7@gmail.com

---

## What this repo is

A single self-contained website file (`index.html`) — all the HTML, styling, and interactivity are in that one file. There's no build step, no framework, and no dependencies to install. Open it in a browser and it works. Edit the file and the change is live.

This is intentional: a marketing site this size doesn't need React or a build pipeline, and keeping it in one file means either of us can edit it from anywhere without setting up tools.

---

## How to edit the site

You can edit directly in the browser — no software needed:

1. Open the repo and click `index.html`
2. Click the **pencil icon** (top-right of the file view)
3. Make your change
4. Scroll down and click **Commit changes** with a short message describing what you did

The change goes live at the URL in about 30 seconds.

**Finding what to change:** use `Ctrl+F` (or `Cmd+F`) inside the editor to jump to one of the `EDIT:` labels below.

---

## EDIT label map

Search the file for these labels to find each editable section:

| Label | What it controls |
|---|---|
| `EDIT:NAV` | Navigation tab labels |
| `EDIT:HOME` | Homepage hero text + the three "what we do" cards |
| `EDIT:ABOUT` | About / mission copy and the "what we stand for" values |
| `EDIT:SESSIONS` | Session cards — dates, prices, feature lists |
| `EDIT:RESOURCES` | Free resource cards + their status labels |
| `EDIT:TEAM` | Bios, credential tags, and photos |
| `EDIT:CONTACT` | Email, Instagram, and Linktree links |
| `EDIT:BOOKING` | The booking form + where to plug in payments |

---

## Common edits, step by step

### Change the colour theme
All colours live in the `:root` block near the top of the `<style>` section. Each colour is a named variable (e.g. `--gold`, `--terra`, `--espresso`). Change one value and it updates everywhere it's used. This is how you re-skin the whole site without hunting through the file.

### Set session prices
Find `EDIT:SESSIONS`. In each session card, replace:
```
<span class="tbd">Price TBD</span><span class="note">/ announced soon</span>
```
with something like:
```
<span class="tbd">$30</span><span class="note">/ per seat</span>
```

### Add a team photo
Find `EDIT:TEAM`. Replace the photo placeholder `<div class="photo">...</div>` with:
```
<img src="jacob.jpg" alt="Jacob Hailemariam" class="photo" style="object-fit:cover;">
```
Upload the photo file to the repo (same place you upload `index.html`) so the filename matches.

### Add Instagram / Linktree links
Find `EDIT:CONTACT` and search for `href="#"`. Replace the `#` with the real URLs. There's also a Linktree placeholder in the nav.

### Publish a free resource
Find `EDIT:RESOURCES`. Change a card's status from `Coming July 2026` to `Available now`, and wrap the card in a link so it's clickable:
```
<a href="link-to-your-pdf.pdf"> ... existing card ... </a>
```

---

## Turning on payments

Right now the **Book a Session** button opens the visitor's email app with their details pre-filled, sent to enginquire7@gmail.com. No payment is taken — pricing isn't set yet.

When we're ready to charge, the `submitBooking()` function in the `<script>` section (look for `EDIT:BOOKING`) has a full comment block explaining three options:

- **Stripe Payment Link** *(recommended)* — free Stripe account, one link per session, swap one line so the button sends people to checkout. Stripe handles receipts and payouts.
- **Google Form** — free, collects sign-ups into a shared sheet, no payment.
- **E-transfer** — keep the email flow and send Interac instructions in the reply.

---

## First-time setup (GitHub Pages hosting)

If the site isn't live yet:

1. **Settings → Pages**
2. Under **Branch**, choose `main` and `/ (root)`, then **Save**
3. Wait 1–2 minutes — the live URL appears at the top of that same page
4. Put that URL at the top of this README

For a custom domain (e.g. `enginquire.com`) later: buy the domain (~$12/yr), then **Settings → Pages → Custom domain** has a one-click guide. Do this only after we've validated demand — the free URL is fine to launch with.

---

## Working together without breaking things

- **One person edits at a time.** Send a quick message before you start editing so we don't both save the same lines at once (that causes a "merge conflict" that's annoying to untangle).
- **Every commit is a restore point.** If something breaks, go to the repo's commit history, find the last good version, and restore it. You can't permanently break the site.
- **Write real commit messages** — "updated Tom's bio", "added Session 1 price" — not "update" or "asdf". It makes the history readable, and it's a good habit for the app work later.

---

## Roadmap

- [ ] Confirm session venue (ESS / on-campus)
- [ ] Finalize session pricing → update site
- [ ] Add team photos
- [ ] Add Instagram + Linktree URLs
- [ ] Turn on Stripe payment links before launch
- [ ] Publish free resources through the summer
- [ ] (Later) Evaluate the app phase after validating demand from the live sessions

---

*Calgary, AB · Built by Jacob & Tom · 2026*
