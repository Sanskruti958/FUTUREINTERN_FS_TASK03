# FUTUREINTERN_FS_TASK03
WORKING CAFE WEBSITE
📌 Project Overview
PeachyBites Café is a local café in Pune, Maharashtra specialising in handcrafted waffles, fresh fruit bowls, and authentic bubble teas. This website was built as a real-world web development project to help the business establish an online presence, attract new customers, and compete with digitally-present competitors.
DetailInfo🏪 Business TypeCafé / Dessert Restaurant📍 LocationBaner, Pune, Maharashtra🛠️ Tech StackHTML5, CSS3, Vanilla JavaScript📱 ResponsiveYes — Mobile, Tablet, Desktop⚡ DependenciesGoogle Fonts (Playfair Display, DM Sans)🌐 HostingGitHub Pages (free)🎨 Color ThemeCream · Peach · Orange · Waffle Gold · Bubble Tea Brown

✨ Features
🧭 Navigation

Fixed sticky navbar with frosted glass blur effect
Smooth scroll to all sections
Active section highlight on scroll
"Order Now" CTA button with orange glow

🦸 Hero Section

Full-viewport hero with waffle-grid CSS background pattern
Dual radial gradient (waffle gold + bubble tea pink)
4 floating food cards (staggered layout, hover lift)
Key stats: 50+ items · 4.9★ rating · 3 years serving
Primary + secondary CTA buttons

📖 Our Story

Two-column layout with café photo
Floating "100% Fresh Daily" badge
3 USP feature rows with emoji icons

🍽️ Menu Section

Filterable menu grid — All · Waffles · Fruit Bowls · Bubble Tea · Pancakes
Each card: real Unsplash food photo, tag badge (Popular / New / Veg), description, ₹ price
Animated "Add" button with green ✓ confirmation
Cart toast notification (bottom-right slide-up)

🧋 Bubble Tea Special

Dark walnut/brown section with peach radial glow overlay
6 flavour chips with colour-coded dots
Dual image layout with depth shadows

🖼️ Gallery

CSS Grid masonry — 1 large hero image + 4 smaller tiles
Hover scale + dark gradient overlay with label reveal

💬 Testimonials

3 customer review cards with star ratings
Avatar initials circles, customer name & tag

📍 Hours & Location

Opening hours table (Mon–Fri / Sat / Sun)
4 contact info chips (address, phone, email, Instagram)
Google Maps placeholder with "Open in Maps" button

📣 CTA Banner

Full-width orange section with emoji food ticker
Direct tel: link for one-tap phone reservation

🔻 Footer

4-column grid: brand + menu links + visit links + newsletter signup
Email subscription input with join button
Social media icon buttons


🗂️ File Structure
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

Note: The current build is a single index.html file — all CSS is in <style> tags and JS is in a <script> tag at the bottom. No build tools, no npm, no frameworks required.


🎨 Design System
Color Palette
VariableHexUsage--cream#FFF8F0Page background--peach-light#FFE8D6Card backgrounds, chips--peach#FFBA8CAccents, flavor dots--orange#F97316Primary buttons, CTA--orange-dark#C2410CHover states, prices--waffle-gold#E8A038Logo accent, stars--bubble-tea#D4A5A5Bubble tea section tint--text-dark#2D1A0EHeadings, body text--text-mid#6B4226Subheadings, labels--text-light#A07050Descriptions, hints
Typography
RoleFontWeightDisplay / HeadingsPlayfair Display400, 700, 900Body / UIDM Sans300, 400, 500, 600
Spacing Scale

Section padding: 90px 5%
Card gap: 24px
Component gap: 16px
Inner padding: 12px–20px


🚀 Getting Started
Option 1 — Open Locally (Instant)
bash# No installation needed — just open the file
open index.html
# or double-click index.html in your file explorer
Option 2 — Deploy to GitHub Pages (Free Hosting)
bash# Step 1: Create a new GitHub repository
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
Option 3 — Deploy to Netlify (Drag & Drop)

Go to netlify.com → Log in
Drag your index.html file onto the deploy zone
Get a live URL instantly (e.g. https://peachy-bites.netlify.app)

Option 4 — Deploy to Vercel
bashnpm i -g vercel
cd peachy-bites
vercel
# Follow the prompts — live in under 30 seconds

🧩 JavaScript Functionality
1. Scroll Reveal Animation
javascript// Uses IntersectionObserver to trigger .visible class
// Elements with .reveal class fade + slide up on scroll
const observer = new IntersectionObserver(entries => {
  entries.forEach(e => {
    if (e.isIntersecting) e.target.classList.add('visible');
  });
}, { threshold: 0.1 });
2. Menu Category Filter
javascript// filterMenu(category, buttonElement)
// Toggles display of .menu-item cards by data-cat attribute
// Categories: 'all' | 'waffle' | 'fruit' | 'bubble' | 'pancake'
function filterMenu(cat, btn) { ... }
3. Add to Cart Toast
javascript// Triggered by the + button on each menu card
// Button turns green ✓ → toast slides up → resets after 2s
function addToCart(btn) { ... }
4. Active Nav Highlight
javascript// Listens to window scroll
// Highlights the matching nav link based on visible section
window.addEventListener('scroll', () => { ... });

📱 Responsive Breakpoints
BreakpointLayout Changes> 900pxFull desktop — 2-column grids, hero visual cards, full nav≤ 900pxTablet — single column, hero cards hidden, hamburger nav≤ 600pxMobile — single column gallery, footer stacked, second bubble image hidden

🖼️ Image Credits
All images sourced from Unsplash (free for commercial use):
ImageUnsplash IDSectionFruit Bowl1567620905732-2d1ec7ab7445Hero card, MenuWaffles1488477181946-6428a0291777Hero card, Menu, GalleryBubble Tea1553361371-9b22f78e8b1dHero card, Menu, GalleryPancakes1565958011703-44f9829ba187Hero card, Menu, GalleryCafé Interior1414235077428-338989a2e8c0About sectionStrawberry Waffle1550617931-e17a7b70dce2Menu, Gallery (hero)French Toast1484723091739-30a097e8f929GalleryAçaí Bowl1490474418585-ba9bad8fd0eaMenu, GalleryBubble Tea 21578914029738-f9aa6a9acfa2Bubble sectionBubble Tea 31556679343-c7306c1976bcBubble section

To use your own photos: replace any https://images.unsplash.com/photo-{ID} URL with a local path like ./assets/images/waffle.jpg


🔧 Customisation Guide
Change Business Name
html<!-- In nav, footer, and page title -->
<div class="nav-logo">Your<span>CafeName</span></div>
<title>Your Café Name — Tagline Here</title>
Change Colors
css/* In :root at top of <style> block */
:root {
  --orange: #F97316;      /* Change to your brand color */
  --orange-dark: #C2410C; /* Darker shade of brand color */
  --cream: #FFF8F0;       /* Background */
}
Add Menu Items
html<!-- Copy this block into #menu-grid -->
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
Update Contact Info
html<!-- In the location section -->
<div class="contact-chip">📍 Your Address Here</div>
<div class="contact-chip">📞 Your Phone Number</div>
<div class="contact-chip">📧 your@email.com</div>
<div class="contact-chip">📸 @yourhandle</div>

<!-- Update the phone CTA link too -->
<a href="tel:+91XXXXXXXXXX" class="cta-white">📞 Reserve a Table</a>
Embed Real Google Maps
html<!-- Replace the .map-placeholder div with: -->
<iframe
  src="https://maps.google.com/maps?q=YOUR+ADDRESS&output=embed"
  width="100%" height="320" style="border:0; border-radius:20px;"
  allowfullscreen loading="lazy">
</iframe>

📊 Business Pitch Summary
Problem
PeachyBites had no online presence. Customers couldn't find them via Google Search, couldn't browse the menu before visiting, and had no easy way to share the café with friends.
Solution
A professional, fast-loading website that:

✅ Shows the full menu with photos and prices
✅ Builds trust through testimonials and gallery
✅ Drives footfall with a clear address and hours
✅ Enables one-tap phone calls for reservations
✅ Grows social following via Instagram link
✅ Captures email leads via newsletter signup

Business Impact
MetricBeforeAfter (Projected)Google discoverability❌ None✅ IndexableOnline menu availability❌ None✅ 24/7Reservation methodPhone onlyPhone + WebSocial proof visible❌ Hidden✅ Public reviewsCustomer reachWalk-in onlyWalk-in + Digital

🧑‍💻 Skills Demonstrated

Semantic HTML5 structure
Advanced CSS (Grid, Flexbox, custom properties, pseudo-elements)
CSS animations & transitions (scroll reveal, hover states, toasts)
IntersectionObserver API for scroll-triggered effects
JavaScript DOM manipulation (filter, toggle, classList)
Responsive design (3 breakpoints, mobile-first thinking)
Real-world UX decisions (sticky nav, cart feedback, section CTAs)
Client communication & business problem framing
Deployment via GitHub Pages


📄 License
This project is open source and available under the MIT License.
Feel free to fork, adapt, and use for your own café, restaurant, or food business pitch.

👤 Author
Built by: Sanskruti Anil Pawar
Course / Project: Real-World Web Development — Business Website Pitch

Year: 2025

"The best way to learn web development is to build something real, for someone real."


<p align="center">Made with 🍑 and lots of bubble tea · Pune, India</p>
