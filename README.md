# Astro Portfolio Website

A bold, responsive personal portfolio built with **Astro**, vanilla JavaScript, and CSS. It is designed for students, developers, and early-career professionals who want a fast static website that can be deployed to GitHub Pages.

## Quick start

```bash
npm install
npm run dev
```

Local site: `http://localhost:4321`

## Customize the portfolio

Most portfolio content lives in:

```text
src/data/profile.js
```

Update the name, role, summary, projects, achievements, skills, email, and social links there.

Replace the public assets with your own files:

- Profile image in `public/assets/`
- Resume PDF in `public/resume/`
- Favicon at `public/favicon.svg`

If you rename those files, also update the matching paths in `src/data/profile.js`.

## Deploy to GitHub Pages

For a GitHub user site URL like:

```text
https://your-username.github.io
```

name the repository:

```text
your-username.github.io
```

Then deploy:

1. Push this project to the repository.
2. Go to **Settings → Pages**.
3. Set **Source** to **GitHub Actions**.
4. Push to `main` or `master`.

The workflow in `.github/workflows/deploy.yml` will build and deploy the site.

For a project site instead of a user site, update the Astro `site` and `base` settings in `astro.config.mjs` to match your repository URL.

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

## Project structure

- `src/data/profile.js` - portfolio content and links
- `src/pages/index.astro` - main page markup, styles, and form behavior
- `src/layouts/BaseLayout.astro` - base HTML document metadata
- `public/assets/` - public images
- `public/resume/` - public resume files
- `.github/workflows/deploy.yml` - GitHub Pages deployment workflow
