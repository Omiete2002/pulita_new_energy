PULITA NEW ENERGY: WEBSITE (www.pulitaenergy.com)
==================================================

A six-page, fully responsive static website for Pulita New Energy Co., Ltd.
Built with HTML5, CSS3 (Tailwind CSS + custom styles) and vanilla JavaScript.
No frameworks, no build step, no server code.


1. HOW TO OPEN THE SITE LOCALLY
-------------------------------
Option A: double-click
  Unzip the folder and double-click index.html. It opens in your browser.
  Everything works offline: fonts, styles, scripts and images are all local.
  (The Google Map on contact.html and WhatsApp/email links need internet.)

Option B: local web server (recommended for testing, closest to live hosting)
  In a terminal, inside the unzipped folder, run ONE of:
      python3 -m http.server 8000
      npx serve .
  Then visit http://localhost:8000

Publishing: upload the entire folder (keep the structure) to any static host,
e.g. cPanel/FTP web hosting, Netlify, Vercel, Cloudflare Pages or GitHub Pages.
index.html is the home page.


2. FOLDER STRUCTURE
-------------------
index.html        Home: hero, LPG/CNG vs diesel comparison, savings calculator,
                  product carousel, Why Pulita, local support, projects, trust bar
about.html        Company story, counters, mission & vision, global map,
                  quality-control timeline, certificates, team
products.html     Product grid with detail pop-ups, full LPG/CNG spec table with
                  kVA finder, tube skids & refill stations, dual-fuel,
                  solar hybrid (interactive diagram), vehicle conversion kits
projects.html     Filterable project gallery (12 Nigerian projects) and the
                  Burger King Abeokuta case study
services.html     After-sales service, process, gas station EPC, quote form
contact.html      Direct contacts, offices, Google Map, contact form
README.txt        This file

assets/css/tailwind.css   Tailwind CSS utilities (pre-compiled, minified)
assets/css/styles.css     Brand components, animations, responsive rules
assets/js/main.js         All interactions (see section 4)
assets/fonts/             Barlow & Barlow Condensed (SIL Open Font License)
assets/images/            All images (see section 6)


3. BRAND
--------
Primary Blue  #004B87    Secondary Red  #E31E24    Accent Gray  #F2F2F2
Text Dark     #1A1A1A    White          #FFFFFF
Display font: Barlow Condensed (echoes the brochure's condensed headlines)
Body font:    Barlow


4. FEATURES
-----------
- Savings calculator (Home): sliders for diesel L/h, hours/day, days/month;
  CNG/LPG toggle; editable fuel prices. Uses Pulita's 100 kW reference data:
  25 L/h diesel is treated as equal to 22.08 kg/h LPG or 30 m3/h CNG.
  Default prices: Diesel N1,300/L, LPG N750/kg, CNG N380/m3 (brochure values).
  To change defaults: edit the value="..." on #price-diesel, #price-lpg,
  #price-cng in index.html.
- Animated LPG/CNG vs diesel bars with per-kWh / per-hour toggle.
- Touch-friendly product carousel (swipe, arrow buttons, mouse drag, keyboard).
- Product detail pop-ups (products.html); the "Request a Quote" button
  pre-selects the product in the quote form.
- kVA finder on the spec table: type a load, the right genset is highlighted.
- Filterable projects gallery with hover/tap overlays.
- Floating WhatsApp button on every page: Nigeria (0803 080 0999) and
  factory/export desk (+86 186 7806 0186).
- Scroll-triggered animations (Intersection Observer), animated counters,
  hover micro-interactions, smooth page transitions. All animations respect
  the visitor's "reduce motion" setting.

FORMS: This is a static site with no server. When a visitor submits a form,
it is validated and then opens WhatsApp (to 0803 080 0999) or the visitor's
email app (to john@hitepower.com) with the enquiry pre-filled.
To receive submissions directly in an inbox instead, connect a form service
(e.g. Formspree, Netlify Forms, Basin): give each <form data-enquiry> an
action="..." URL and method="post", and remove the submit handler block
marked "Forms" in assets/js/main.js.

TAILWIND: tailwind.css is pre-compiled so the site works offline and loads
fast. If you prefer the Tailwind Play CDN, replace the tailwind.css <link> in
each page's <head> with:  <script src="https://cdn.tailwindcss.com"></script>
(the line is already noted in a comment in every page).


5. CONTENT TO CONFIRM BEFORE GOING LIVE
---------------------------------------
Search the HTML for "EDIT:" to find these spots.
  a) about.html, "The team behind your power": the three portraits show
     placeholder names/roles ("Team member name" / "Role · Office").
     Replace them with the correct names and titles.
  b) contact.html, Abuja Office: no street address was supplied.
     Add the address (an EDIT comment marks the spot).
  c) Mission and vision wording (about.html) is draft copy. Please review.
  d) No client testimonial is shown because none was supplied. Add an approved
     quote from Burger King (or another client) to the "Project spotlight"
     on index.html if you get one in writing.
  e) Fuel prices in the calculator and comparison use the brochure's reference
     prices. Update them as market prices change.
  f) Burger King wording follows public launch coverage, which called it
     "Burger King Nigeria's first green restaurant" (not "Nigeria's first").


6. ASSETS USED
--------------
Supplied photos and logo (converted from WebP and optimised):
  pulita-logo.png                         Pulita logo (header/footer)
  favicon.png                             Browser icon cut from the logo
  pulita-generator-blue.png               Blue soundproof LPG/CNG generator
  pulita-generator-soundproof-beige.png   Beige silent-canopy generator
  factory-production-line-white-generators.jpg   Factory floor, white gensets
  engineer-laptop-blue-generator.jpg      Engineer with laptop, blue genset (Home hero)
  team-containerized-unit.jpg             Team at containerized unit
  nog-energy-week-team.jpg                Team at NOG Energy Week
  team-portrait-1.jpg / -2.jpg / -3.jpg   Team portraits

Cropped from the supplied brochure PDF:
  pulita-logo-large.jpg                   Large logo (structured data)
  factory-weifang-exterior.jpg            Weifang factory exterior & sign
  factory-gallery-1.jpg, -2.jpg, -5.jpg   Factory/workshop photos
  quality-control-testing.jpg             QC inspector at control panel
  iso-certificate-1.jpg (ISO 14001), -2.jpg (ISO 45001), -3.jpg (ISO 9001)
  cng-generator-open-orange.jpg           Open-type CNG engine genset
  cng-generator-container-white.jpg       White containerized CNG genset
  lpg-generator-open-type.jpg             Open-type LPG genset
  dual-fuel-generator.jpg                 Dual-fuel (diesel-gas) genset
  cng-cylinder-group.jpg                  CNG cylinder cascade
  prms-unit.jpg                           PRMS pressure regulating unit
  cng-tube-skid-trailer.jpg               CNG tube skid trailer
  mobile-daughter-station-open.jpg        Daughter station, doors open
  mobile-daughter-station-dispenser.jpg   Daughter station with dispenser
  gas-station-epc-1.jpg / -2.jpg          Gas station EPC photos
  cng-conversion-kit-diagram.jpg          Vehicle conversion kit diagram
  solar-off-grid-inverters.jpg            Off-grid inverter series
  pv-module-580w.jpg                      580 W PV module
  hybrid-site-1.jpg ... -4.jpg            PV + storage installation photos
  project-*.jpg (12 files)                Nigerian project case photos

Generated for the site:
  world-map-dots.svg                      Dotted world map (Natural Earth data)

Note: the brochure's project photos are small (about 410 px wide), so they
are used at card size. Higher-resolution originals would sharpen the
Projects page.

No third-party stock images were needed. All imagery is Pulita's own.

(c) Pulita New Energy Co., Ltd.
