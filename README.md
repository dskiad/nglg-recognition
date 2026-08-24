# NGLG Recognition

Two standalone HTML files — no build step, no dependencies.

| File | What it is |
|---|---|
| [`builder.html`](builder.html) | **NGLG Recognition Builder** — the authoring tool. |
| [`regularity-2026august.html`](regularity-2026august.html) | **NGLG Regularity.0** — the rendered August 2026 edition (preview). |
| [`index.html`](index.html) | Landing page linking to both. |

## Live preview

Published with GitHub Pages:

- Landing: `https://dskiad.github.io/nglg-recognition/`
- Builder: `https://dskiad.github.io/nglg-recognition/builder.html`
- Preview: `https://dskiad.github.io/nglg-recognition/regularity-2026august.html`

## Running locally

Just open the files in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000

## Publishing an update

Export from the builder with **⬇ Download HTML**, then:

```bash
cd ~/nglg-recognition && ./publish.sh
```

It picks up the newest `.html` in `~/Downloads`, shows you what it found, asks
for confirmation, then commits, pushes, and waits for the Pages build.

```bash
./publish.sh path/to/file.html                 # publish a specific file
./publish.sh file.html regularity-2026sep.html # publish as a new edition
./publish.sh -y                                # skip the confirmation
```

Note: the builder's **Save** button stores versions in your browser (IndexedDB)
only — they are not in this repo. **Download HTML** is the portable copy.
