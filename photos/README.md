# Product photos

The site looks for one image per product at:

```
photos/<brand>/<model>.jpg
```

Brand folders (already created):

- `photos/kenstar/`
- `photos/maharaja-whiteline/`
- `photos/magppie/`

## How the filename is built

The site turns each product name into the filename automatically:
lowercase, and every run of spaces or punctuation becomes a single `-`.

| Product | File to add |
|---|---|
| Kenstar → Matrix 2000W Steam Iron | `photos/kenstar/matrix-2000w-steam-iron.jpg` |
| Maharaja Whiteline → Ultramax Elite | `photos/maharaja-whiteline/ultramax-elite.jpg` |
| Magppie → Triply Kadhai | `photos/magppie/triply-kadhai.jpg` |

The full list of every expected filename is in **`manifest.csv`** in this
folder — open it, and the `expected_file` column is exactly what to name
each photo.

## Rules

- **Extension must be `.jpg`** (lowercase). If you only have PNGs, either
  re-save as `.jpg`, or change the extension in `index.html` — search for
  `.jpg` inside the `photoSrc` function near the top of the script.
- **Square-ish images work best.** Cards crop to a 4:3 window, centred.
  1000×750 px or 1200×1200 px is plenty; keep each file under ~300 KB.
- **A missing photo is safe.** If a file isn't there yet, that card shows
  the line-drawing icon instead of breaking. Add photos whenever you get
  them; no code change needed.
- Filenames are case-sensitive on GitHub Pages. Keep everything lowercase.

## Pushing to GitHub

Commit this whole `photos/` folder along with the site. The `.gitkeep`
files keep the empty brand folders in the repo so the paths resolve even
before you've added every photo.
