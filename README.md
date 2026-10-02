# App Privacy Center

Static GitHub Pages site hosting privacy policies for our Play Store apps.


## Structure

```
index.html            → hub listing all apps
assets/css/style.css  → shared styles
assets/css/theme-sky.css → dark-sky theme override (opt-in: <body class="sky-theme">)
ciphora/              → Privacy Policy for Ciphora (com.ciphora.app)
skivon/               → Privacy Policy for Skivon (com.skivon.skivon) — uses theme-sky.css
_template/            → copy-paste starter for the next app
404.html
.nojekyll             → serve as plain static site
```

## Themes

`style.css` is the shared light theme. To give an app its own look, add an opt-in
override stylesheet and add the class to that app's `<body>`:

- `skivon/index.html` links `theme-sky.css` and uses `<body class="sky-theme">`
  (deep navy sky, glass surfaces, light-blue accents — matches the Skivon app UI).

## Add a new app

1. Copy `_template/` → e.g. `my-new-app/`
2. Edit `my-new-app/index.html` (name, package, data practices, contact email)
3. Add a card in root `index.html` linking to `my-new-app/`
4. Commit & push

## Publish with GitHub Pages

1. Push this folder as a GitHub repo (e.g. `privacy-policy-for-apps`)
2. Repo → Settings → Pages → Deploy from branch → `main` / root
3. Use the Pages URL in Play Console:
   - Ciphora: `https://<username>.github.io/<repo>/ciphora/`
   - Skivon: `https://<username>.github.io/<repo>/skivon/`
   

