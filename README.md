# Terry's Moving Sale 🏷️

A static website for listing items for sale, built with [Jekyll](https://jekyllrb.com/) and hosted on [GitHub Pages](https://pages.github.com/).

Live site: **https://ttferreira.github.io/terrys-moving-sale/**

---

## Features

- 🗂️ **Category-based browsing** — filter items by category with a single click
- 📄 **Detailed listing pages** — each item has its own page with images, description, specs, and useful links
- 💰 **Clear pricing** — price prominently displayed on cards and detail pages
- ✉️ **One-click enquiry** — "I'm Interested!" button pre-fills an email to the seller
- 📱 **Responsive design** — works great on mobile, tablet, and desktop

---

## Adding a New Item

1. Create a new Markdown file in the `_items/` directory (e.g. `_items/my-item.md`).
2. Add the following front matter at the top of the file:

```yaml
---
title: "My Item Name"
category: "Electronics"          # Category label shown in filters
price: 150                       # Asking price in dollars (number, no $ sign)
original_price: 399              # Optional — original retail price
condition: "Good"                # Optional — Like New / Excellent / Good / Fair
description: "A short description of the item shown on the card and listing page."
images:
  - "/terrys-moving-sale/assets/images/my-item-1.jpg"   # First image is the hero
  - "/terrys-moving-sale/assets/images/my-item-2.jpg"   # Additional thumbnails
specs:
  Brand: "Acme"
  Colour: "Black"
  Year: "2022"
links:
  - label: "Product page"
    url: "https://example.com/product"
---

Any extra notes or details written here in Markdown will appear in the
"Additional Details" section at the bottom of the listing page.
```

3. Add any images to `assets/images/` and reference them in the `images` list.
4. Commit and push — GitHub Pages will rebuild the site automatically.

### Available Categories

| Category | Badge Colour |
|---|---|
| Electronics | Blue |
| Furniture | Purple |
| Kitchen & Appliances | Green |
| Outdoor & Garden | Amber |
| Sports & Recreation | Red |
| Books & Media | Pink |

Any new category name you use will automatically appear in the filter bar.

---

## Local Development

Requires Ruby and Bundler. Run:

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000/terrys-moving-sale/ in your browser.

---

## GitHub Pages Setup

1. Go to **Settings → Pages** in your repository.
2. Set the source to the `main` branch (or whichever branch you use), root directory.
3. GitHub will build and deploy the site automatically.

If your repository is not at `TTFerreira/terrys-moving-sale`, update the `baseurl` and `url` values in `_config.yml`.
