# Academic website

A plain HTML/CSS site. It needs no build step and works on GitHub Pages as-is.

## Files

| Path | What it is |
|---|---|
| `index.html` | All page content. Look for `EDIT:` comments |
| `style.css` | Look and feel. Change `--accent` to recolour the site |
| `assets/profile.svg` | Placeholder photo. Replace with `profile.jpg` and update the `<img>` in `index.html` |
| `assets/favicon.svg` | Browser-tab icon. Change "YN" to your initials |
| `files/cv.pdf` | Your CV |
| `files/projects/` | Project reports, slides and theses (PDF) |
| `files/papers/` | Paper PDFs (only ones you're allowed to share) |
| `files/talks/` | Talk slides |

## Adding a project

1. Put the PDF in `files/projects/`, using a name without spaces such as `my-project.pdf`.
2. In `index.html`, copy one `<article class="card"> … </article>` block in the Projects section.
3. Edit the year, title, description and tags, and set the link to `files/projects/my-project.pdf`.

## Publishing on GitHub Pages

1. On GitHub, create a **public** repository named exactly `<your-username>.github.io`.
2. In this folder, run:
   ```bash
   git init
   git add .
   git commit -m "Initial website"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```
3. On GitHub, go to the repository's **Settings → Pages**. Set **Source** to *Deploy from a branch* and choose **main / (root)**.
4. The site goes live at `https://<your-username>.github.io` within a minute or two.

## Updating the site later

```bash
git add .
git commit -m "Add new project"
git push
```

## Previewing locally

Open `index.html` in your browser, or run `python -m http.server` in this folder and visit http://localhost:8000.
