# Asia Trip Journal

A static multi-page website about an Asia trip. It is dependency-free and can be hosted for free on GitHub Pages.

## Pages

- `index.html` — overview and trip framing.
- `itinerary.html` — week-by-week timeline.
- `countries.html` — country summaries.
- `gallery.html` — Asia-only photo gallery.

## Local preview

```bash
python -m http.server 4173 --bind 127.0.0.1
```

Then open `http://127.0.0.1:4173/`.

## Super beginner guide: publish to GitHub Pages

If you are new to branches, use this mental model:
- A **repository** is your project folder on GitHub.
- A **branch** is a version line of that project.
- Your main branch is usually named **`main`** (sometimes `master`).
- This project is already configured to auto-deploy when you push to `main` or `master`.

### 1) Create the GitHub repo (once)

1. Go to GitHub and create a new repository named `test1`.
2. Keep it public (simplest for GitHub Pages).
3. Do **not** add a README from the GitHub website (you already have one here).

### 2) Connect your local project to GitHub (once)

Run these commands in this project folder:

```bash
git remote add origin https://github.com/<your-github-username>/test1.git
git branch -M main
git push -u origin main
```

What this does:
- `git remote add origin ...` links your local code to your GitHub repo.
- `git branch -M main` ensures your default branch is named `main`.
- `git push -u origin main` uploads your files to GitHub.

### 3) Turn on GitHub Pages in the GitHub UI (once)

1. Open your GitHub repo page.
2. Click **Settings**.
3. Click **Pages** in the left sidebar.
4. Under **Build and deployment**, set **Source** to **GitHub Actions**.

That is it. You do not need to manually pick a branch for deployment in this setup, because the workflow file does it automatically.

### 4) Wait for first deploy (1–3 minutes)

1. Click the **Actions** tab in your repo.
2. Open the latest run named **Deploy static site to GitHub Pages**.
3. Wait until it shows a green checkmark.

### 5) Open your live site

For your repo/user values, your URL should be:

`https://noahknopf-coder.github.io/test1/`

## Updating the website later (easy workflow)

Any time you change files:

```bash
git add .
git commit -m "Update site content"
git push
```

Pushing to `main` will trigger a fresh GitHub Pages deploy automatically.

## Troubleshooting (quick)

- If your URL shows 404 right after setup, wait 2–5 minutes and refresh.
- If Actions fails, open the failed run and read the red error step.
- If you accidentally used another branch, push your changes to `main`.

## URL format reference

- Project pages repo: `https://<your-github-username>.github.io/<repo-name>/`
- User pages repo: `https://<your-github-username>.github.io/`
