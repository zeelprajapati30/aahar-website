# AAHAR — Healthy Food, Happy Life

A complete, responsive **static frontend** for the AAHAR cloud kitchen, using the supplied logo and food posters as the visual source. Includes interactive CSS-3D bowl tilting, floating ingredients, subscription plans, working basket, and WhatsApp order request flow.

## How to run on Windows

1. Extract the entire ZIP to a folder.
2. Double-click `START-WEBSITE.bat` (or `index.html`).
3. Browse the website. Add bowls or plans to the cart; fill in delivery details; click **Send order request on WhatsApp** to open the prepared message.

**No Node.js, npm, build or internet connection is needed to open the site.** An internet connection is needed for Google Fonts, Instagram and WhatsApp handoff. System fonts are used when Google Fonts are unavailable.

## Included features

- Responsive homepage, menu, ingredient story, plans, FAQ, contact details
- CSS 3D-style bowl tilt, parallax hover, orbiting/decorative food, smooth animation, reduced-motion support
- Weekly and monthly pricing switcher with all eight offers (2 singles + 6 plans)
- Persistent basket (localStorage), quantity controls and subtotal
- Customer details and prefilled WhatsApp order request
- Real supplied imagery cropped from your posters and original provided logo
- Delivery disclosure, order cutoff timings and contact links

## Important limitations

- **3D appearance is simulated using layered photographs and CSS perspective, not a downloadable Three.js 3D mesh.** This keeps the project self-contained and offline runnable. Real 3D ingredient models can be added in a later phase.
- This is a **frontend website, not a production commerce backend**. It doesn't store customer orders on a server, take payments, authenticate users, or automatically accept orders.
- WhatsApp requests are not submitted until the customer presses **Send** in WhatsApp, and availability/delivery/payment need manual confirmation.
- Combos explicitly include delivery. Single-bowl delivery is shown as ₹20. The delivery charge for Paneer-only/Mexican-only plans remains unconfirmed.
- Please verify all menu prices, business numbers, ingredients, delivery service area, actual nutrition claims and Instagram before launching.
- Customer names/addresses are held in the browser form and passed into the WhatsApp URL when the customer requests an order. Don't treat this static app as a HIPAA or other regulated backend.

## Files

- `index.html` — site structure and content
- `style.css` — responsive styling and animation
- `script.js` — menu plans, basket and ordering
- `images/` — logo and food images
- `vercel.json` — Vercel config (caching)
- `START-WEBSITE.bat` — Windows launcher

## Deploy on Vercel

1. Upload this folder to GitHub (or drag-drop in Vercel dashboard / run `vercel` CLI).
2. Framework Preset: **Other**. Leave Build Command and Output Directory **empty**.
3. Deploy. Images load from `/images/...` — no `public` folder is used, so nothing breaks.

## Run on desktop

Double-click `START-WEBSITE.bat` or `index.html`. All paths are relative, so it works offline (except Google Fonts).
