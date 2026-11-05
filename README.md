# TEEDUH — Dressed for the heat

Student project by **Studio Empat** (4 members). A sales website for TEEDUH, a fictional Singapore street-style label sold on Shopee and Lazada. The site is built with HTML and CSS only (no JavaScript).

## Pages (15 main pages + 12 product pages)

After professor feedback the site was cut from 19 to 15 main pages so the menus are simpler: the style guide now lives in the Lookbook (`lookbook.html#style-guide`), sustainability in Fabric (`fabric.html#sustainability`), shipping and returns in the FAQ (`faq.html#delivery-returns`), and New arrivals links go to Shop.

| Menu | Pages |
| --- | --- |
| Home | index.html |
| Shop | shop.html, women.html, men.html, size-guide.html |
| Products | air-shirt.html, breeze-pant.html, rose-tee.html, stripe-knit.html, dot-tank.html, tie-top.html, sheer-dress.html, wrap-skirt.html, suede-skirt.html, zip-jacket.html, pleat-henley.html, drift-shorts.html |
| Discover | lookbook.html (with style guide), fabric.html (with sustainability), journal.html, community.html |
| About | about.html, contact.html, team.html |
| Help | faq.html (with shipping & returns) |
| CTA | get-15-off.html (voucher form + PDPA consent) |
| Extra | privacy.html, 404.html (shown by GitHub Pages for broken links) |

## The collection (Drop 03, street style)

| Piece | Fit | Price | Colours |
| --- | --- | --- | --- |
| The Air Shirt | Unisex | S$59 | Blue Stripe, Light Grey, White |
| The Breeze Pant | Women | S$65 | Espresso |
| Rose Wash Tee | Unisex | S$35 | Washed Black |
| Stripe Knit Polo | Unisex | S$55 | Dark Stripe, Light Stripe |
| Dot Lace Tank | Women | S$39 | Black Dot, Blue Dot |
| Off-Shoulder Tie Top | Women | S$42 | Dark, Sorbet, Grey |
| Pleat Sheer Dress | Women | S$69 | Black |
| Wrap Maxi Skirt | Women | S$52 | Black, White |
| Suede Panel Skirt | Women | S$62 | Tan, Bone |
| Suede Zip Jacket | Unisex | S$79 | Espresso, Marble |
| Pleat Henley Top | Unisex | S$45 | Charcoal |
| Drift Shorts | Unisex | S$39 | Black |

## Interactivity (CSS only)
- White tile "peel" transition on every page load
- Black marquee announcement bar
- Header: "Collections" mega menu (hover on desktop, tap on mobile) with link columns and two photo cards; on the home page the header is clear over the hero and turns frosted after it
- Home: full-screen hero that the next sections slide over; three grey product slides (arrows or tap the faded next product, radio buttons) with colour swatches that swap the product photo; product rails that scroll sideways; a jacket that opens as you scroll and reveals the story inside (scroll-driven animation); floating "Buy on Shopee" bar
- Shop pages: Category, Fit and Sort panels (HTML `popover`), active filter chips, "Showing X of Y" count, Large / Medium / Small grid switch
- Product cards: hover swaps to the street-style photo; the "+" button reveals quick sizes
- Product pages: colour and size pickers that swap the photo, accordions, "You may also like" slider, sticky buy bar on mobile
- Auto-scrolling Instagram mix-and-match strip above the footer: all ten supplied looks on shared pages, with five matching looks on each Women/Men page
- Size-guide tabs, FAQ accordion (`<details>`), lookbook hover reveal, dismissible cookie notice

## Before you submit
1. **Forms**: create a free form at https://formspree.io and replace `your-form-id` in `get-15-off.html` and `contact.html`.
2. **Store links**: replace `https://shopee.sg/` and `https://www.lazada.sg/` with your product's real listing URLs (keep the `?utm_...` part for tracking).
3. **Photos**: catalogue cards, hover images, product galleries, homepage product slides, and collection-menu photos use the supplied Drunk Dad images in `images/catalog/`. `images/catalog/source-map.json` records each original product, image, and source collection. Women and Men pages follow those collection labels; shared pieces are marked Unisex, with collection-appropriate or product-only alternate photos.
   The ten supplied AI-generated styling concepts in `images/instagram/` (optimized as WebP, same dimensions and framing; sources in `images/instagram/source-map.json`) are used for the Instagram strips, the community gallery, the home hero (three photos side by side), the photos inside the jacket reveal, the lookbook, the style guide, the journal, and the About and Sustainability pages. The Fabric page uses the Air Shirt close-up from `images/catalog/`.
   The jacket fronts in the home-page reveal are drawn in CSS (no image files). The old mannequin placeholders (`hero.jpg`, `reveal-*.jpg`, `look-*.jpg`, `journal-*.jpg`, `about-studio.jpg`, `sustainability.jpg`, `fabric-macro.jpg`) are no longer used by any page. To use your own campaign photo somewhere, change the `src` in that page instead.
4. **Fabric page**: the comparison bars are illustrative. Replace them with your own test results.

## Publish on GitHub Pages
1. Create a new public repository on GitHub, for example `teeduh`.
2. Upload every file and folder from this zip, so that `index.html` sits at the top level.
3. Go to **Settings → Pages**, set Source to "Deploy from a branch", pick `main` and `/ (root)`, then click Save.
4. After a minute or two, the site is live at `https://<your-username>.github.io/teeduh/`.

## Design system
- Layout and look follow the Hanzify "Lite 001" Shopify theme (used as a temporary design reference)
- Colours: Ink #111111, Text #333333, Mute #6E6E73, Card grey #F2F2F4, Slide grey #F6F6F6, Line #E6E6E6, Black #000000, White #FFFFFF
- Fonts: Archivo (logo, headlines, marquee), Inter (product names, prices, buttons), Work Sans (body text), all from Google Fonts
- All styles are in `css/style.css`. Change the variables in `:root` to re-theme the whole site.
- Browser support: the jacket reveal, the header colour change, the floating bar and the rail arrows use newer CSS (`:has()`, `popover`, scroll-driven animations, `::scroll-button`). Current Chrome and Edge support all of them. Other browsers get a simpler version that still works (for example, the jacket section shows the inside photo and text straight away, and rails scroll by swipe or trackpad).
