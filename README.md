# Sushant Singh — Portfolio

Personal portfolio site for [sushantsingh.com.np](https://sushantsingh.com.np), hosted on GitHub Pages with a custom domain routed through Cloudflare DNS.

## Live pages

| Page | File | Description |
|---|---|---|
| Home | `index.html` | Landing page — bio, social links, blog embed, YouTube videos, donate CTA |
| Games | `game.html` | 4 playable mini-games (Snake, 2048, Memory Match, Reflex Tap) |
| Music | `music.html` | Spotify playlist/album embeds |
| Blog | external | Links out to [lifeofsushanttt.blogspot.com](https://lifeofsushanttt.blogspot.com/) |

## Tech stack

- Plain HTML, CSS, and vanilla JavaScript — no build step, no frameworks, no dependencies
- Fonts: [Outfit](https://fonts.google.com/specimen/Outfit) (headings) and [Inter](https://fonts.google.com/specimen/Inter) (body) via Google Fonts
- Games page also uses [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) for score labels
- Live chat via [Tawk.to](https://www.tawk.to/)
- Contact via `mailto:` link (Formspree used elsewhere in earlier iterations)

## Design

Light-blue glassmorphism aesthetic shared across all pages:
- Frosted-glass cards (`backdrop-filter: blur()`) over a soft sky gradient background
- Pill-shaped floating header with a nav menu (Blog / Games / Music) that stays fixed on scroll
- Consistent color tokens defined as CSS custom properties (`--accent`, `--ink`, `--glass-fill`, etc.) at the top of each page's `<style>` block — edit these to reskin the whole page at once
- Fully responsive down to mobile, with reduced-motion support for the floating background bubbles

## File structure

```
.
├── index.html      # Home page
├── game.html       # Mini-games page
├── music.html       # Spotify embeds page
├── photo.jpg        # Profile photo (used as avatar + favicon)
└── README.md
```

> Note: `index.html` links to `song.html` in its footer ("Test site") — add that file or update/remove the link if it's not part of the live site.

## Setup

1. Clone or download this repo.
2. Add your own `photo.jpg` in the repo root (used for the avatar and browser tab favicon).
3. Update personal details as needed:
   - Social links in the "Find me around the web" section of `index.html`
   - Blog embed URL (`iframe src`) in `index.html`
   - YouTube video IDs in the `video-grid` section of `index.html`
   - Email address in the `mailto:` link
   - Donate link (currently points to the Prime Minister Disaster Relief Fund, Nepal)
4. Add your Spotify embeds to `music.html` — see the instructions in the comment block above the `.embed-slot` sections.

## Deployment (GitHub Pages + Cloudflare)

This site is deployed via GitHub Pages and mapped to a custom domain (`sushantsingh.com.np`) using Cloudflare DNS.

1. Push this repo to GitHub.
2. In the repo, go to **Settings → Pages** and set the custom domain to your domain (or subdomain).
3. In Cloudflare, add a **CNAME** record pointing your domain/subdomain to `<your-github-username>.github.io`, with the proxy status set to **DNS only** (grey cloud) — GitHub Pages' SSL certificate issuance is unreliable behind Cloudflare's proxy.
4. Wait for DNS to propagate, then enable **Enforce HTTPS** in GitHub Pages settings once available.

## License

Personal project — feel free to use the structure/layout as a reference, but please don't reuse the personal content, photos, or branding as-is.
