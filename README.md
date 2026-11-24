# RePix-VFI project page

Source of the project page for **RePix-VFI: Re-rendering Observed Pixels for Video Frame Interpolation with Generative
Priors from One-Step Diffusion** (Dayeon Kim, Jeonghyeok Do, Munchurl Kim; KAIST; arXiv preprint, 2026).

- Live page: https://kaist-viclab.github.io/RePix-VFI_site/
- Code repository: https://github.com/KAIST-VICLab/RePix-VFI

The page is plain HTML, CSS and JavaScript with no build step and no dependencies other than Google Fonts.
GitHub Pages serves it from the repository root (`.nojekyll` turns off Jekyll processing).

## Preview locally

Serve the folder over HTTP rather than opening `index.html` from disk, so that every path resolves as it does on GitHub Pages:

```bash
cd RePix-VFI_site
python3 -m http.server 8000
# then open localhost:8000 in a browser
```

## Layout

```
index.html                the page: comparison videos (x16, x8), the reconstruction stages, paper figures,
                          quantitative results, method overview and BibTeX
static/css/family.css     styles shared with the other KAIST-VICLab family pages (the same file on each)
static/js/family.js       scripts shared with those pages: navigation, abstract toggle, pending links, BibTeX copy,
                          image lightbox, tabs, table scroll cues
static/css/style.css      RePix-VFI colours (top of the file), video cards, switchers, video strips and table extras
static/js/main.js         video cards (loaded and played only when shown), switchers, video lightbox
static/videos/            the demo videos: <name>.mp4, its poster <name>.jpg (first frame) and thumbnail <name>_thumb.jpg
static/images/            paper figures: *_1200.jpg / *_2000.jpg are inline, *_full.jpg open in the lightbox;
                          og.jpg (social preview) and the logo files
static/paper/RePix-VFI.pdf  the paper (PDF), opened by the Paper button and the navigation bar's Paper link
```

## Videos

The fifteen videos are the authors' renderings, unchanged (only the index was moved to the front of each file, so
playback starts while it downloads). Each one shows a 2 x 4 grid, with the full frame above and a fixed enlarged crop
below in every column: the overlaid bounding keyframes, FILM, GIMM-VFI, MoMo, SPEED, LDF-VFI, RePix-VFI and the ground
truth (the reconstruction stages for the DAVIS car-turn video of Fig. 4). Each video plays its window three times: in
real time (24 fps), then 3x and 6x slower.

## Logo and colours

`static/images/logo.svg` (the hero title), `icon.svg` (navigation and footer) and `icon_square.svg` are the authors' logo
files; `favicon-32.png`, `favicon-64.png` and `apple-touch-icon.png` are made from the square icon. The logo's pink
`#FF0066` is the colour of RePix-VFI in the paper's Fig. 1; the page uses a calmer shade of it for accents (`#E8317A`)
and deeper ones for small text (`#C41862`). Filled areas use `#EAF7FD`, the light blue of the paper's highlighted table
rows. All colours are set at the top of `static/css/style.css`.

## arXiv link

The arXiv identifier is not set yet. Until it is, the arXiv button, the footer's arXiv link and the BibTeX entry carry a
placeholder identifier; such a link is shown as pending (the arXiv button carries a "soon" badge) and does not navigate.
Setting the identifier in `index.html` is enough; no CSS or JavaScript file needs editing. The Paper button and the
navigation bar's Paper link open the hosted PDF, `static/paper/RePix-VFI.pdf`.
