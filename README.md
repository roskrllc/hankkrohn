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
| `README.md` | This file |

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
