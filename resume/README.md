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

## Deploying to Netlify

1. Go to [netlify.com](https://netlify.com) and log in with GitHub
2. Click **Add new site → Import an existing project → GitHub**
3. Select the `toloughlin/claude` repository
4. Build settings:
   - **Base directory:** `resume`
   - **Build command:** *(leave blank)*
   - **Publish directory:** `resume`
5. Click **Deploy site**
6. Add your custom domain `tomsresu.me` under **Domain management** in the site settings
