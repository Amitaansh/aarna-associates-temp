# Aarna Associates — website

Single-page distributor site. No build step, no dependencies. Just static
files you can push straight to GitHub Pages.

## Files

```
index.html            the whole site
favicon.svg           tab icon (crisp, modern browsers)
favicon.ico           tab icon (older browsers)
favicon-16.png        \
favicon-32.png         }  PNG fallbacks
apple-touch-icon.png  /   home-screen icon on iPhone/iPad
icon-192.png          \
icon-512.png           }  Android / PWA install icons
site.webmanifest      app metadata (name, colours, icons)
photos/               product images  ->  see photos/README.md
```

## Deploy on GitHub Pages

1. Create a repo (e.g. `aarna-site`) and push all of these files to the
   root of the `main` branch.
2. Repo → **Settings → Pages** → Source: **Deploy from a branch**,
   Branch: **main**, Folder: **/ (root)** → Save.
3. It goes live at `https://<username>.github.io/<repo>/` in a minute.

For the real domain, add a file named `CNAME` at the root containing
`aarnaassociates.com`, then point the domain's DNS at GitHub Pages.

## Adding products or photos

- **Photos:** drop images into `photos/<brand>/` — filenames are listed in
  `photos/manifest.csv`. Full guide in `photos/README.md`.
- **Products:** each item is one line in the `P` array near the top of the
  `<script>` in `index.html`. Copy a line, change the fields.

## Contact details to confirm

`index.html` currently shows the WhatsApp line **9690900444** on every
"Ask for rate" button and the office line **7017808591** with address
**60 Tyagi Road, Dehradun**. Change these in the contact section and the
`WA` constant in the script if anything is off.
