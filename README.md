# Upendra Kulshrestha — Academic Website

A personal academic website for **Dr. Upendra Kulshrestha**, Assistant Professor, Automobile
Engineering, Manipal University Jaipur. Plain HTML/CSS, no build step, no external framework —
just upload and go.

## Structure

```
index.html           Home — bio, research interests, news
cv.html               Curriculum vitae — education, employment, memberships, competency, certifications
research.html         Research areas, industry/research projects, workshops organized
publications.html     Journal publications + conference proceedings
teaching.html         Teaching positions, course expertise, certifications
talks.html            Workshops & conferences organized / attended
assets/css/main.css   Stylesheet (self-contained, no external theme dependency)
```

Icons come from Font Awesome (CDN). Fonts (Space Grotesk / IBM Plex Sans / IBM Plex Mono) load
from Google Fonts (CDN). No local font or image files are required to view the site.

## How to publish this on GitHub Pages

1. Create a new GitHub repository — e.g. `ukulshrestha.github.io` (a repo named exactly
   `<your-username>.github.io` gives you a root-domain site; any other name works too, served at
   `<username>.github.io/<repo>`).
2. Upload/push all the files in this folder to the repository, keeping the folder structure
   (`index.html`, `cv.html`, ..., `assets/css/main.css`).
3. In the repo, go to **Settings → Pages**, and set:
   - Source: `Deploy from a branch`
   - Branch: `main` (or `master`), folder `/ (root)`
4. Save. GitHub publishes the site at `https://<your-username>.github.io/` (or
   `/<repo-name>/` if the repo isn't named `<username>.github.io`) within a minute or two.

### Quick push from the command line

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

## Editing content

Every page is a self-contained HTML file — open it in any text editor and edit directly.
- Update your bio, contact details, and news items in `index.html`.
- Add publications by copying a `<li>` inside the `<ol class="pub-list">` block in
  `publications.html`.
- Add CV entries (education, employment, memberships) by copying a `.cv-entry` block in `cv.html`.
- Colors, fonts, and spacing all live in `assets/css/main.css` if you want to tweak the look —
  the palette variables are defined at the top of the file (`--steel`, `--brass`, `--paper`, etc.).

## Optional: add a profile photo

The current design uses a simple monogram badge ("UK") instead of a photo. To swap in a real
photo, drop an image at `images/profile.jpg` and replace the `.badge` block in each page with:

```html
<img src="images/profile.jpg" alt="Upendra Kulshrestha" style="width:100%;border-radius:50%;">
```
