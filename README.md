# Six Cards: Business Cards That Open Doors

A single-file, static marketing and order site for a custom business card and brand design service. Visitors browse card styles, preview a QR code, send a request, and are pointed to Venmo once their mockup is approved.

**Tagline:** *A card that opens doors.*

---

## Features

- **Winter collection (6 styles):** Frost, Aurora, Pine, Snowdrift, Midnight, Hearth. Frost, Aurora and Pine include a QR code; Snowdrift, Midnight and Hearth are left clear. A QR can be added to any style.
- **Archives library (12 styles):**
  - *Audience series:* Storefront, Handle, Club, Notebook, Maker, Stage
  - *Original series:* Executive, Cobalt, Ivory, Sage, Blush, Slate
- **Audience sections:** businesses vs. job seekers/creators, plus promotion paths for shops, social profiles and clubs/organizations.
- **Free QR preview tool:** paste a link, pick a color, generate, and download a PNG.
- **10 add-on services:** QR codes and link pages, custom ads, posters, logo design, social media starter kit, flyers and handouts, banners and signage, menus and price lists, brand style guide, email signature and digital card.
- **Promotion tips:** six practical recommendations for getting more from each card.
- **Request form:** style buttons preselect the form dropdown and scroll to the contact section.
- **Venmo payment flow:** after a successful submit, the form is replaced with a confirmation panel and a pay button.
- **Accessibility and polish:** sticky blurred nav, scroll-reveal animations, `prefers-reduced-motion` support, and responsive layouts down to mobile.

## Deliverables

Every card ships as double-sided, print-ready **300 DPI** files sized for **3.5" × 2"** cards, with printing instructions. Same-day pickup is available depending on location; shipping is also offered.

## Tech stack

| Piece | Details |
|---|---|
| Markup / styling | Plain HTML and CSS in one file (`index.html`), no build step |
| Fonts | Google Fonts: Cormorant Garamond, Share Tech Mono |
| QR codes | [qrcodejs 1.0.0](https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js) via cdnjs |
| Form handling | [FormSubmit](https://formsubmit.co) (AJAX endpoint, with a normal form POST as fallback) |
| Payments | Venmo profile link (`@sixcardsonline`) |

## Project structure

```
.
├── index.html   # the entire site: CSS, markup and JS
└── README.md
```

Page sections, in order: **Hero → Audiences → Promote → Winter styles → QR studio → Library (Archives) → Services → Process → Promotion tips → Pay → Contact → Footer**

## Running locally

No install required. Open `index.html` in a browser, or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

The QR preview, fonts and form need an internet connection.

## Deployment

Any static host works: GitHub Pages, Netlify, Vercel, Cloudflare Pages, or a plain web server. Upload `index.html` and you're done.

## Customizing

- **Colors:** edit the CSS variables in `:root` at the top of the stylesheet.
- **Add a card style:**
  1. Add a `.mini.yourname` CSS block.
  2. Add a `.style-card` in the relevant section (Winter or Library).
  3. Add a matching `<option>` in the `#f-style` dropdown.
  4. Optionally add a `.t-yourname` tagline color class.
- **Add a service:** copy a `.svc` card in `#services` and add a matching `<option>` under "More services".
- **Contact email:** update it in the form `action`, the AJAX `fetch` URL, and the `mailto:` link.
- **Venmo handle:** update the `VENMO_URL` constant in the script, plus the handle text and link in the `#pay` section.
- **Nav links:** the nav lists every section anchor; update it if you add or remove sections.

## Form setup note

FormSubmit requires a one-time email confirmation. After deploying, submit a test request and click the activation link sent to the receiving address; until then, submissions won't be delivered.

## Order flow

1. Visitor picks a style or service and sends a request.
2. Owner replies by email with a mockup and final price.
3. Visitor approves and pays via Venmo, noting their name and card style.
4. Print-ready 300 DPI front and back files are sent, usually within hours.

## License

© 2026 Zachary Frederic. All rights reserved.# SIX·CARDS — Business Cards That Open Doors

Custom business card design for companies building their brand — and for people building their careers. Six signature styles, print-ready files, printing instructions included.

**Live site:** [zachc0des.github.io/sixcards](https://zachc0des.github.io/sixcards/)

---

## What It Is

Six Cards is a design service site built and run by [Zachary Frederic](https://zachc0des.github.io). Every card ships as double-sided, print-ready **300 DPI** files sized for standard **3.5" × 2"** cards, with printing steps included — same-day pickup where available, or shipped to your door.

Two audiences, one system:

- **For businesses** — landscaping crews, salons, gyms, food trucks, freelancers. A card that makes a one-person operation look like an institution: logo, services, and pricing hook on one clean card, with bulk-friendly layouts that match your flyers, invoices, and social banners.
- **For job seekers & creators** — interviews, career fairs, networking events. Name, title, and skill tags styled like a portfolio, with links to your GitHub, LinkedIn, or content pages. Pairs with your resume — same fonts, same identity.

## The Six Signature Styles

| Style | Look | Best For |
|---|---|---|
| **The Executive** | Ink black · brass spine — classic authority | Trades, local shops, client-facing brands |
| **The Cobalt** | Night navy · circuit grid — modern edge | Tech, job seekers, creators, digital brands |
| **The Ivory** | Warm white · ruled lines — quiet luxury | Consultants, planners, boutiques, formal fields |
| **The Sage** | Soft green · dot grid — calm & natural | Wellness, salons, coaches, eco & care work |
| **The Blush** | Blush & plum · pinstripe — warm welcome | Beauty, events, creators, hospitality |
| **The Slate** | Cool gray · corner ticks — pure minimal | Corporate, finance, law, anyone who wants clean |

Don't see your vibe? **Fully custom cards** can be built from scratch — your colors, your logo, your idea.

## How It Works

1. **Reach out** — send your name or business, what you do, and your contact details.
2. **Pick a style** — six looks to choose from; the layout, colors, and tags get tailored to you.
3. **Get your files** — print-ready 300 DPI front & back, sized for standard cards.
4. **Print your way** — same-day pickup where available, or ship to your door. Steps included.

## Built With

- **HTML / CSS / JavaScript** — single-page static site, no frameworks
- **GitHub Pages** — free hosting straight from this repo
- Fully responsive, designed to preview all six card styles in-browser

## Repo Structure

```
sixcards/
├── index.html    # Full site — markup, styles, and scripts
└── README.md     # This file
```

## Run Locally

```bash
git clone https://github.com/Zachc0des/sixcards.git
cd sixcards
# open index.html in a browser, or serve it:
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Contact & Ordering

Requests go straight through the contact form on the [live site](https://zachc0des.github.io/sixcards/), or write directly:

- **Email:** [digitalshiftdynamics@gmail.com](mailto:digitalshiftdynamics@gmail.com)
- **Portfolio:** [zachc0des.github.io](https://zachc0des.github.io)
- **GitHub:** [@Zachc0des](https://github.com/Zachc0des)

---

© 2026 Zachary Frederic · Six signature styles · One custom
