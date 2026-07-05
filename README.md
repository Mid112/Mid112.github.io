# Mridul Nohria — Portfolio

A bold, playful personal website for an early-career software developer. Built with **Astro**, vanilla JavaScript, and CSS. Designed for GitHub Pages.

## Quick start

```bash
npm install
npm run dev
```

Local site: `http://localhost:4321`

## Deploy to GitHub Pages

For the clean URL `https://mid112.github.io`, create or rename the repository to:

```text
Mid112.github.io
```

Then:

1. Push this project to the repository.
2. Go to **Settings → Pages**.
3. Set **Source** to **GitHub Actions**.
4. Push to `main` or `master`.

The workflow in `.github/workflows/deploy.yml` will build and deploy the site.

## Contact form email setup

This portfolio uses Web3Forms so the contact form can send messages from a static GitHub Pages site.

1. Create a Web3Forms access key using the email where you want messages delivered.
2. In your GitHub repo, go to **Settings → Secrets and variables → Actions**.
3. Add a repository secret:

```text
PUBLIC_WEB3FORMS_ACCESS_KEY = your_access_key_here
```

4. Re-run the GitHub Actions deployment.

Without this key, the form will show a warning and the direct email link will still work.

## Editing content

Most text lives in:

```text
src/data/profile.js
```

Update projects, links, achievements, skills, email, phone, and social links there.

## Files included

- Profile image: `public/assets/mridul-nohria.png`
- Resume PDF: `public/resume/Mridul_Nohria_Resume.pdf`
- Main page: `src/pages/index.astro`
- Deployment workflow: `.github/workflows/deploy.yml`
