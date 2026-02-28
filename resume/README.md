# tomsresu.me

Static resume site for [tomsresu.me](https://tomsresu.me) — Thomas J. O'Loughlin, Senior Systems & Storage Infrastructure Engineer.

Zero dependencies. Single self-contained HTML file with embedded CSS, vanilla JS, and CDN-loaded fonts.

## Structure

```
resume/
├── index.html          # The entire site — HTML, CSS, JS in one file
├── assets/
│   └── headshot/       # Place headshot photo here when ready
└── README.md
```

## Adding the headshot

1. Place your photo in `assets/headshot/` (e.g., `assets/headshot/headshot.jpg`)
2. In `index.html`, find the headshot section in the hero and make two changes:
   - Uncomment the `<img>` tag
   - Remove (or comment out) the `<div class="headshot-placeholder">` block

```html
<!-- Before -->
<div class="headshot-wrap">
  <!-- <img src="assets/headshot/headshot.jpg" alt="Thomas J. O'Loughlin" /> -->
  <div class="headshot-placeholder">...</div>
</div>

<!-- After -->
<div class="headshot-wrap">
  <img src="assets/headshot/headshot.jpg" alt="Thomas J. O'Loughlin" />
</div>
```

## Deploying to Cloudflare Pages

1. Push this repo to GitHub
2. In the [Cloudflare Dashboard](https://dash.cloudflare.com), go to **Workers & Pages → Create → Pages → Connect to Git**
3. Select this repository
4. Build settings:
   - **Build command:** *(leave blank)*
   - **Build output directory:** `/`
5. Deploy — Cloudflare will serve `index.html` directly
6. Add your custom domain `tomsresu.me` under **Custom domains** in the Pages project settings
