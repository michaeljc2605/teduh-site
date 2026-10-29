# TEDUH — Dressed for the heat

Student project by **Studio Empat** (4 members). A sales website for TEDUH, a fictional Singapore street-style label sold on Shopee and Lazada. The site is built with HTML and CSS only (no JavaScript).

## Pages (20 + Privacy Policy)

| Menu | Pages |
| --- | --- |
| Home | index.html |
| Shop | shop.html, women.html, men.html, new.html, air-shirt.html, breeze-pant.html, size-guide.html |
| Discover | lookbook.html, fabric.html, style-guide.html, journal.html, sustainability.html, community.html |
| About | about.html, contact.html, team.html |
| Help | faq.html, shipping.html |
| CTA | get-15-off.html (voucher form + PDPA consent) |
| Extra | privacy.html |

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
- Auto-scrolling Instagram strip above the footer on every page
- Size-guide tabs, FAQ accordion (`<details>`), lookbook hover reveal, dismissible cookie notice

## Before you submit
1. **team.html**: replace the group number, tutorial group, names and emails.
2. **Forms**: create a free form at https://formspree.io and replace `your-form-id` in `get-15-off.html` and `contact.html`.
3. **Store links**: replace `https://shopee.sg/` and `https://www.lazada.sg/` with your product's real listing URLs (keep the `?utm_...` part for tracking).
4. **Photos**: catalogue cards, hover images, product galleries, homepage product slides, and collection-menu photos use the supplied Drunk Dad images in `images/catalog/`. `images/catalog/source-map.json` records each original product, image, and source collection. Women and Men pages follow those collection labels; shared pieces are marked Unisex, with collection-appropriate or product-only alternate photos. Other campaign, editorial, and community images are still placeholders. To replace those, save a photo over the placeholder **with the exact same file name**. Suggested shapes:
   - `hero.jpg` and `reveal-inside.jpg`: landscape (e.g. 2400 × 1350). The hero title sits in the centre
   - `reveal-left.jpg` and `reveal-right.jpg`: the two halves of a closed jacket front (zipper on the inside edge), 960 × 1080 each
   - `community-*.jpg`: Instagram posts, portrait 4:5
   - `look-*.jpg`: tall 9:14 (e.g. 1350 × 2100)
   - `banner-women.jpg`, `banner-men.jpg` (menu cards), `about-studio.jpg`, `sustainability.jpg`: portrait 4:5
   - `journal-*.jpg`: landscape 16:10; `fabric-macro.jpg`: landscape; `og-image.jpg`: 1200 × 630
5. **Fabric page**: the comparison bars are illustrative. Replace them with your own test results.

## Publish on GitHub Pages
1. Create a new public repository on GitHub, for example `teduh`.
2. Upload every file and folder from this zip, so that `index.html` sits at the top level.
3. Go to **Settings → Pages**, set Source to "Deploy from a branch", pick `main` and `/ (root)`, then click Save.
4. After a minute or two, the site is live at `https://<your-username>.github.io/teduh/`.

## Design system
- Layout and look follow the Hanzify "Lite 001" Shopify theme (used as a temporary design reference)
- Colours: Ink #111111, Text #333333, Mute #6E6E73, Card grey #F2F2F4, Slide grey #F6F6F6, Line #E6E6E6, Black #000000, White #FFFFFF
- Fonts: Archivo (logo, headlines, marquee), Inter (product names, prices, buttons), Work Sans (body text), all from Google Fonts
- All styles are in `css/style.css`. Change the variables in `:root` to re-theme the whole site.
- Browser support: the jacket reveal, the header colour change, the floating bar and the rail arrows use newer CSS (`:has()`, `popover`, scroll-driven animations, `::scroll-button`). Current Chrome and Edge support all of them. Other browsers get a simpler version that still works (for example, the jacket section shows the inside photo and text straight away, and rails scroll by swipe or trackpad).
