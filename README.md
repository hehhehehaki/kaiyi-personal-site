# Kaiyi — A Little World

A personal homepage built with HTML, CSS, and vanilla JavaScript. No framework, build step, or package installation is needed.

## Files

- `index.html`: page content and structure.
- `styles.css`: colors, typography, layout, and responsive styles.
- `script.js`: the journey category filter.
- `assets/profile.jpg`: the Shiba Inu photo from my earlier website.
- `PRACTICE.md`: a step-by-step learning guide.

## Run locally

Download and unzip the project, then open `index.html` in your browser. Keep the other files beside it. For live editing, open the folder in VS Code and use a local preview extension, or run `python -m http.server 8000` in this folder if Python is installed, then visit http://localhost:8000.

## Customize

Change the text in `index.html`. Edit the variables at the top of `styles.css` to change the palette. Replace `assets/profile.jpg` to use another photo. The category buttons work by matching `data-filter` with each entry’s `data-category`.

## Put it on GitHub manually

1. Sign in to GitHub and create a repository such as `kaiyi-personal-site`.
2. Choose public or private according to your preference.
3. Select **Add file → Upload files**.
4. Upload the files inside this project folder, including the `assets` folder. Do not upload only the ZIP.
5. Commit the upload. The repository now holds your source and practice guide.

Optional command-line route, after creating an empty repository:

```bash
git init
git add .
git commit -m "Add personal homepage and learning guide"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/kaiyi-personal-site.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your GitHub username. Use GitHub’s authentication flow; never put a token into these files.

## Template or hand coding?

This version was written directly in HTML, CSS, and JavaScript with AI assistance. It does not use the Bootstrap resume template from my old site. You can reuse it as your own starting template, or rebuild it section by section to practice. Understanding and changing the code matters more than starting with an empty file.

The download contains portable source only: no Sites account identifiers, deployment credentials, or service configuration.
