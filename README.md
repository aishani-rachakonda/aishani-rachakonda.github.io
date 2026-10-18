# aishani-rachakonda.github.io

My personal portfolio website, built with plain HTML and CSS and hosted on GitHub Pages.

```
index.html                         ← main page content (edit this to update the site)
resume.html                        ← resume page (shows the PDF; no need to edit)
style.css                          ← colors, fonts, layout
assets/Aishani_Rachakonda_Resume.pdf
assets/img/profile.jpg             ← your photo (add this)
```

## Preview locally

From this folder:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Publish on GitHub Pages (one-time setup)

1. **Create the repository.** On GitHub, click **New repository** and name it exactly
   `aishani-rachakonda.github.io` (your username + `.github.io`). Make it **Public**.
   Don't add a README or license, since this folder already has one.

2. **Push this folder** (run these from inside this folder):

   ```bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/aishani-rachakonda/aishani-rachakonda.github.io.git
   git push -u origin main
   ```

3. **Turn on Pages.** In the repo, go to **Settings → Pages**. Under *Build and deployment*, set
   **Source: Deploy from a branch**, **Branch: `main`**, folder **`/ (root)`**, and click **Save**.

4. Wait a minute or two, then visit **https://aishani-rachakonda.github.io**.

## Updating the site

Edit the files, preview locally, then:

```bash
git add .
git commit -m "Describe the change"
git push
```

GitHub Pages redeploys automatically within a minute or two.

### Common edits

- **Add a news item:** copy one `<li>` in the News section of `index.html` and put it at the top.
- **Add a project:** copy one `<article class="project">` block and edit it. Replace the
  `GitHub →` link with the repository URL.
- **Update the resume:** replace `assets/Aishani_Rachakonda_Resume.pdf` with the new file
  (keep the same name). The resume page picks it up automatically.
- **Add a role:** copy one `<article class="role">` block in the Experience section.
- **Add or change your photo:** save a square image as `assets/img/profile.jpg`
  (around 600×600 px). Until it's there, the page shows "AR" initials instead.
- **Change colors or fonts:** edit the variables at the top of `style.css`. After editing
  `style.css`, bump the `?v=2` in the stylesheet link in `index.html` and `resume.html` (to `?v=3`, etc.)
  so browsers load the new version instead of a cached copy.
