# Tutor's Academy — demo website

A single-file static site (`index.html`). No build step, no backend. Everything is in one file.

## Things to fill in later

Search `index.html` for the word **FILL** — there are 3 spots:

1. **"Request a tutor" form link** — replace `href="#"` with the Google Form link for parents/students.
2. **"Register as a tutor" form link** — replace `href="#"` with the Google Form link for tutors.
3. **Contact details** — WhatsApp number(s) and email in the Contact section. Replace the `[ to be added ]` placeholders.

Also replace the **sample openings** in the `<script>` block at the bottom (the `openings` list) with real assignments. Each entry is one opening: number, class, subject, schedule, fee, mode. Later this can be wired to a Google Sheet so the client updates openings without touching the code.

## Google Forms to create (on the client's Google account)

**Form 1 — Request a Tutor** (parents/students): parent name, WhatsApp number, student class, board, subjects, mode (online/home), days per week, preferred time, budget, area/city.

**Form 2 — Tutor Registration** (tutors): name, WhatsApp number, qualification, subjects, classes taught, experience, mode, city/area, expected fee, assignment number (optional).

Responses land in Google Sheets automatically. In each form, turn on **Settings → Responses → Email notifications** so the client gets alerted instantly.

## Hosting on GitHub Pages

1. Create a GitHub repo (e.g. `tutors-academy`).
2. Upload `index.html` to it.
3. Repo **Settings → Pages → Source: Deploy from a branch → main / root → Save**.
4. Site goes live at `https://<username>.github.io/tutors-academy/` within a few minutes.

## Custom domain (client already has one)

In the repo: **Settings → Pages → Custom domain** — enter their domain. Then in their domain registrar's DNS, add a CNAME record pointing `www` to `<username>.github.io`, and the four GitHub Pages A records for the apex domain. Enable "Enforce HTTPS" once it verifies.
