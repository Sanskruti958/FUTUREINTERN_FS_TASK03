# 🍑 PeachyBites Café — Official Website

> A fully responsive, production-grade café website built with pure HTML, CSS & JavaScript. Designed for a real local business pitch with live demo capability.

![PeachyBites Banner](https://images.unsplash.com/photo-1488477181946-6428a0291777?w=1200&h=400&fit=crop)

---

## 🌐 Live Demo

🔗 **[View Live Site](https://Sanskruti950.github.io/peachy-bites/)**  
📁 **[GitHub Repository](https://github.com/Sanskruti950/peachy-bites)**

> _Replace the links above with your actual GitHub Pages URL and repo link after deployment._

---

## 📌 Project Overview

**PeachyBites Café** is a local café in Pune, Maharashtra specialising in handcrafted waffles, fresh fruit bowls, and authentic bubble teas. This website was built as a real-world web development project to help the business establish an online presence, attract new customers, and compete with digitally-present competitors.

| Detail | Info |
|---|---|
| 🏪 Business Type | Café / Dessert Restaurant |
| 📍 Location | Baner, Pune, Maharashtra |
| 🛠️ Tech Stack | HTML5, CSS3, Vanilla JavaScript |
| 📱 Responsive | Yes — Mobile, Tablet, Desktop |
| ⚡ Dependencies | Google Fonts (Playfair Display, DM Sans) |
| 🌐 Hosting | GitHub Pages (free) |
| 🎨 Color Theme | Cream · Peach · Orange · Waffle Gold · Bubble Tea Brown |

---

## ✨ Features

### 🧭 Navigation
- Fixed sticky navbar with frosted glass blur effect
- Smooth scroll to all sections
- Active section highlight on scroll
- "Order Now" CTA button with orange glow

### 🦸 Hero Section
- Full-viewport hero with waffle-grid CSS background pattern
- Dual radial gradient (waffle gold + bubble tea pink)
- 4 floating food cards (staggered layout, hover lift)
- Key stats: 50+ items · 4.9★ rating · 3 years serving
- Primary + secondary CTA buttons

### 📖 Our Story
- Two-column layout with café photo
- Floating "100% Fresh Daily" badge
- 3 USP feature rows with emoji icons

### 🍽️ Menu Section
- **Filterable menu grid** — All · Waffles · Fruit Bowls · Bubble Tea · Pancakes
- Each card: real Unsplash food photo, tag badge (Popular / New / Veg), description, ₹ price
- Animated "Add" button with green ✓ confirmation
- Cart toast notification (bottom-right slide-up)

### 🧋 Bubble Tea Special
- Dark walnut/brown section with peach radial glow overlay
- 6 flavour chips with colour-coded dots
- Dual image layout with depth shadows

### 🖼️ Gallery
- CSS Grid masonry — 1 large hero image + 4 smaller tiles
- Hover scale + dark gradient overlay with label reveal

### 💬 Testimonials
- 3 customer review cards with star ratings
- Avatar initials circles, customer name & tag

### 📍 Hours & Location
- Opening hours table (Mon–Fri / Sat / Sun)
- 4 contact info chips (address, phone, email, Instagram)
- Google Maps placeholder with "Open in Maps" button

### 📣 CTA Banner
- Full-width orange section with emoji food ticker
- Direct `tel:` link for one-tap phone reservation

### 🔻 Footer
- 4-column grid: brand + menu links + visit links + newsletter signup
- Email subscription input with join button
- Social media icon buttons

---

## 🗂️ File Structure

```
peachy-bites/
│
├── index.html          ← Complete single-file website (HTML + CSS + JS)
├── README.md           ← This file
│
└── assets/             ← (Optional) if you move to multi-file setup
    ├── css/
    │   └── style.css
    ├── js/
    │   └── main.js
    └── images/
        └── (local images if replacing Unsplash URLs)
```

> **Note:** The current build is a single `index.html` file — all CSS is in `<style>` tags and JS is in a `<script>` tag at the bottom. No build tools, no npm, no frameworks required.

---

## 🎨 Design System

### Color Palette

| Variable | Hex | Usage |
|---|---|---|
| `--cream` | `#FFF8F0` | Page background |
| `--peach-light` | `#FFE8D6` | Card backgrounds, chips |
| `--peach` | `#FFBA8C` | Accents, flavor dots |
| `--orange` | `#F97316` | Primary buttons, CTA |
| `--orange-dark` | `#C2410C` | Hover states, prices |
| `--waffle-gold` | `#E8A038` | Logo accent, stars |
| `--bubble-tea` | `#D4A5A5` | Bubble tea section tint |
| `--text-dark` | `#2D1A0E` | Headings, body text |
| `--text-mid` | `#6B4226` | Subheadings, labels |
| `--text-light` | `#A07050` | Descriptions, hints |

### Typography

| Role | Font | Weight |
|---|---|---|
| Display / Headings | Playfair Display | 400, 700, 900 |
| Body / UI | DM Sans | 300, 400, 500, 600 |

### Spacing Scale
- Section padding: `90px 5%`
- Card gap: `24px`
- Component gap: `16px`
- Inner padding: `12px–20px`

---

## 🚀 Getting Started

### Option 1 — Open Locally (Instant)
```bash
# No installation needed — just open the file
open index.html
# or double-click index.html in your file explorer
```

### Option 2 — Deploy to GitHub Pages (Free Hosting)

```bash
# Step 1: Create a new GitHub repository
# Go to github.com → New Repository → Name: peachy-bites

# Step 2: Clone and add files
git clone https://github.com/yourusername/peachy-bites.git
cd peachy-bites
cp /path/to/index.html .
cp /path/to/README.md .

# Step 3: Push to GitHub
git add .
git commit -m "🍑 Initial commit — PeachyBites Café website"
git push origin main

# Step 4: Enable GitHub Pages
# GitHub repo → Settings → Pages → Branch: main → Folder: / (root) → Save
# Live in ~60 seconds at: https://yourusername.github.io/peachy-bites/
```

### Option 3 — Deploy to Netlify (Drag & Drop)
1. Go to [netlify.com](https://netlify.com) → Log in
2. Drag your `index.html` file onto the deploy zone
3. Get a live URL instantly (e.g. `https://peachy-bites.netlify.app`)

### Option 4 — Deploy to Vercel
```bash
npm i -g vercel
cd peachy-bites
vercel
# Follow the prompts — live in under 30 seconds
```

---

## 🧩 JavaScript Functionality

### 1. Scroll Reveal Animation
```javascript
// Uses IntersectionObserver to trigger .visible class
// Elements with .reveal class fade + slide up on scroll
const observer = new IntersectionObserver(entries => {
  entries.forEach(e => {
    if (e.isIntersecting) e.target.classList.add('visible');
  });
}, { threshold: 0.1 });
```

### 2. Menu Category Filter
```javascript
// filterMenu(category, buttonElement)
// Toggles display of .menu-item cards by data-cat attribute
// Categories: 'all' | 'waffle' | 'fruit' | 'bubble' | 'pancake'
function filterMenu(cat, btn) { ... }
```

### 3. Add to Cart Toast
```javascript
// Triggered by the + button on each menu card
// Button turns green ✓ → toast slides up → resets after 2s
function addToCart(btn) { ... }
```

### 4. Active Nav Highlight
```javascript
// Listens to window scroll
// Highlights the matching nav link based on visible section
window.addEventListener('scroll', () => { ... });
```

---

## 📱 Responsive Breakpoints

| Breakpoint | Layout Changes |
|---|---|
| `> 900px` | Full desktop — 2-column grids, hero visual cards, full nav |
| `≤ 900px` | Tablet — single column, hero cards hidden, hamburger nav |
| `≤ 600px` | Mobile — single column gallery, footer stacked, second bubble image hidden |

---

## 🖼️ Image Credits

All images sourced from **[Unsplash](https://unsplash.com)** (free for commercial use):

| Image | Unsplash ID | Section |
|---|---|---|
| Fruit Bowl | `1567620905732-2d1ec7ab7445` | Hero card, Menu |
| Waffles | `1488477181946-6428a0291777` | Hero card, Menu, Gallery |
| Bubble Tea | `1553361371-9b22f78e8b1d` | Hero card, Menu, Gallery |
| Pancakes | `1565958011703-44f9829ba187` | Hero card, Menu, Gallery |
| Café Interior | `1414235077428-338989a2e8c0` | About section |
| Strawberry Waffle | `1550617931-e17a7b70dce2` | Menu, Gallery (hero) |
| French Toast | `1484723091739-30a097e8f929` | Gallery |
| Açaí Bowl | `1490474418585-ba9bad8fd0ea` | Menu, Gallery |
| Bubble Tea 2 | `1578914029738-f9aa6a9acfa2` | Bubble section |
| Bubble Tea 3 | `1556679343-c7306c1976bc` | Bubble section |

> To use your own photos: replace any `https://images.unsplash.com/photo-{ID}` URL with a local path like `./assets/images/waffle.jpg`

---

## 🔧 Customisation Guide

### Change Business Name
```html
<!-- In nav, footer, and page title -->
<div class="nav-logo">Your<span>CafeName</span></div>
<title>Your Café Name — Tagline Here</title>
```

### Change Colors
```css
/* In :root at top of <style> block */
:root {
  --orange: #F97316;      /* Change to your brand color */
  --orange-dark: #C2410C; /* Darker shade of brand color */
  --cream: #FFF8F0;       /* Background */
}
```

### Add Menu Items
```html
<!-- Copy this block into #menu-grid -->
<!-- data-cat options: waffle | fruit | bubble | pancake -->
<div class="menu-item reveal" data-cat="waffle">
  <img src="YOUR_IMAGE_URL" alt="Item Name">
  <div class="menu-item-body">
    <div class="tag-badge tag-new">✨ New</div>
    <h3>Your Item Name</h3>
    <p>Short description of the item here</p>
    <div class="menu-item-footer">
      <span class="price">₹XXX</span>
      <button class="add-btn" onclick="addToCart(this)">+</button>
    </div>
  </div>
</div>
```

### Update Contact Info
```html
<!-- In the location section -->
<div class="contact-chip">📍 Your Address Here</div>
<div class="contact-chip">📞 Your Phone Number</div>
<div class="contact-chip">📧 your@email.com</div>
<div class="contact-chip">📸 @yourhandle</div>

<!-- Update the phone CTA link too -->
<a href="tel:+91XXXXXXXXXX" class="cta-white">📞 Reserve a Table</a>
```

### Embed Real Google Maps
```html
<!-- Replace the .map-placeholder div with: -->
<iframe
  src="https://maps.google.com/maps?q=YOUR+ADDRESS&output=embed"
  width="100%" height="320" style="border:0; border-radius:20px;"
  allowfullscreen loading="lazy">
</iframe>
```

---

## 📊 Business Pitch Summary

### Problem
PeachyBites had no online presence. Customers couldn't find them via Google Search, couldn't browse the menu before visiting, and had no easy way to share the café with friends.

### Solution
A professional, fast-loading website that:
- ✅ Shows the full menu with photos and prices
- ✅ Builds trust through testimonials and gallery
- ✅ Drives footfall with a clear address and hours
- ✅ Enables one-tap phone calls for reservations
- ✅ Grows social following via Instagram link
- ✅ Captures email leads via newsletter signup

### Business Impact
| Metric | Before | After (Projected) |
|---|---|---|
| Google discoverability | ❌ None | ✅ Indexable |
| Online menu availability | ❌ None | ✅ 24/7 |
| Reservation method | Phone only | Phone + Web |
| Social proof visible | ❌ Hidden | ✅ Public reviews |
| Customer reach | Walk-in only | Walk-in + Digital |

---

## 🧑‍💻 Skills Demonstrated

- Semantic HTML5 structure
- Advanced CSS (Grid, Flexbox, custom properties, pseudo-elements)
- CSS animations & transitions (scroll reveal, hover states, toasts)
- `IntersectionObserver` API for scroll-triggered effects
- JavaScript DOM manipulation (filter, toggle, classList)
- Responsive design (3 breakpoints, mobile-first thinking)
- Real-world UX decisions (sticky nav, cart feedback, section CTAs)
- Client communication & business problem framing
- Deployment via GitHub Pages

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

Feel free to fork, adapt, and use for your own café, restaurant, or food business pitch.

---

## 👤 Author

**Built by:** Your Name  
**Course / Project:** Real-World Web Development — Business Website Pitch  
**College:** Your College Name  
**Year:** 2025  

> _"The best way to learn web development is to build something real, for someone real."_

---

<p align="center">Made with 🍑 and lots of bubble tea · Pune, India</p>
