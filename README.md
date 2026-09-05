# hankkrohn.com

Personal brand site for [Henry (Hank) Krohn](https://hankkrohn.com).

Static HTML and CSS at the repository root. No build step, no framework.

## Pages-ready layout

GitHub Pages should publish from the `main` branch, **root** directory:

| File | Role |
| --- | --- |
| `index.html` | Site |
| `styles.css` | Styles |
| `CNAME` | Custom domain (`hankkrohn.com`) |
| `assets/hank-avatar.jpg` | Primary headshot (hero). Drop Hank’s LinkedIn photo here. |
| `assets/photos/` | Optional field photos (About + Field notes). Missing files hide themselves. |
| `README.md` | This file |

### Photo drop-in paths

Replace or add these files — the HTML/CSS already points at them:

- `assets/hank-avatar.jpg` — primary circular headshot (LinkedIn profile photo)
- `assets/photos/lupines-mountains.jpg` — soft hero wash (`01`)
- `assets/photos/hank-waterfall.jpg` — About, “in the field” (`07`, high priority)
- `assets/photos/moss-canyon.jpg` — Field notes (`02`)
- `assets/photos/crater-lake.jpg` — Field notes (`10`)

Skipped to keep the site sparse: stone textures (`04`–`06`), turquoise-pool (`03`), turquoise-canyon (`09`), lupines-river-cliff (`08`), basalt-columns (`11`), waterfall-flowers (`12`).

Until those optional photos exist, the Field notes strip and About portrait stay hidden. The hero still shows the avatar path above.

The `CNAME` file contains exactly:

```
hankkrohn.com
```

## Enable GitHub Pages

1. Open the repo **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Set the branch to `main` and the folder to `/ (root)`.
4. Save. GitHub will honor the `CNAME` file and serve the site at `https://hankkrohn.com` once DNS is pointed here.

Default GitHub Pages URL (before or alongside the custom domain): `https://roskrllc.github.io/hankkrohn/`.

## DNS

Point **hankkrohn.com** at GitHub Pages:

- Apex: GitHub Pages A records (`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`), or an ALIAS/ANAME if the registrar supports it.
- Optional `www`: CNAME to `roskrllc.github.io`.

In Pages settings, the custom domain should read `hankkrohn.com`. Enable HTTPS after the certificate provisions.

**henrykrohn.com** will redirect to **hankkrohn.com** later via DNS. That redirect is not configured in this repo.

## Local preview

```bash
python3 -m http.server 8080
```

Open [http://localhost:8080](http://localhost:8080).
