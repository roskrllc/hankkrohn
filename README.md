# hankkrohn.com

Personal site for [Henry (Hank) Krohn](https://hankkrohn.com).

Static HTML and CSS at the repository root. No build step, no framework.

Navy field (`#0A1628` / `#0B1C33`) with gold lettering (`#D4AF37` / `#C9A227`). Gold bird mark in the header and favicon.

## Pages-ready layout

GitHub Pages should publish from the `main` branch, **root** directory:

| File | Role |
| --- | --- |
| `index.html` | Site |
| `styles.css` | Styles |
| `CNAME` | Custom domain (`hankkrohn.com`) |
| `assets/gold-bird.png` | Header mark and favicon |
| `assets/hank-avatar.jpg` | Hero headshot |
| `assets/photos/` | Field photos (portrait 3/4, landscape 4/3) |
| `README.md` | This file |

### Photos

- `assets/photos/lupines-mountains.jpg` — hero wash (landscape, 4/3)
- `assets/photos/hank-waterfall.jpg` — Field notes (landscape, 4/3)
- `assets/photos/moss-canyon.jpg` — Field notes (portrait, 3/4)
- `assets/photos/crater-lake.jpg` — Field notes (portrait, 3/4)

Portrait frames use `aspect-ratio: 3 / 4` and `object-fit: cover`. Landscape frames use `4 / 3`. Photos sit under a navy overlay at roughly 0.25–0.45 opacity.

The `CNAME` file contains exactly:

```
hankkrohn.com
```

## Enable GitHub Pages

1. Open the repo **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Set the branch to `main` and the folder to `/ (root)`.
4. Save. GitHub will honor the `CNAME` file and serve the site at `https://hankkrohn.com` once DNS is pointed here.

## DNS

Point **hankkrohn.com** at GitHub Pages:

- Apex: GitHub Pages A records (`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`), or an ALIAS/ANAME if the registrar supports it.
- Optional `www`: CNAME to the GitHub Pages host for this repository.

In Pages settings, the custom domain should read `hankkrohn.com`. Enable HTTPS after the certificate provisions.

## Local preview

```bash
python3 -m http.server 8080
```

Open [http://localhost:8080](http://localhost:8080).
