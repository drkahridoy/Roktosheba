# RoktoSheba (রক্তসেবা) — Implementation Plan

## Product scope
A Bengali-first, mobile-first local healthcare service website for RoktoSheba, a home blood sample collection service operating in Gazipur. The primary conversion is a genuine booking enquiry, with phone and WhatsApp as the fallback because no booking backend is configured.

## Verified business information
- Brand: RoktoSheba (রক্তসেবা)
- Service: Home Blood Sample Collection Service
- Primary service area: Shibbari Mor, Gazipur Sadar, Gazipur, Bangladesh
- Phone: +8801687818128 / 01687818128
- Facebook: https://www.facebook.com/share/19uSe3tFaL/
- Tagline: Safe • Hygienic • Professional

## Design direction
The visual system is modern clinical care: medical blue and white create trust, red is reserved for action and care markers, and green signals hygiene and reassurance. Bengali headings use a high-contrast serif display style with readable Bengali sans-serif body text. The layout uses spacious editorial sections, rounded cards, clear CTA hierarchy, soft blue backgrounds, and an original hero asset placeholder path that will be replaced by the generated image when its managed asset finishes.

## Content and safety decisions
The site explicitly distinguishes sample collection from laboratory testing, avoids unsupported certifications, prices, hours, exact addresses, lab partnerships, reviews, and clinical guarantees, and tells visitors that an enquiry is not a confirmed appointment until the team confirms it. Privacy and terms sections explain the fallback flow and discourage sending NID, passwords, payment-card details, or unnecessary medical information.

## Implementation
- `index.html`: Bengali-first metadata, Open Graph tags, canonical URL, LocalBusiness structured data using only verified information.
- `src/main.js`: single-page semantic content sections covering home, about, services, process, service area, FAQs, booking enquiry, contact, privacy, and terms; mobile navigation, FAQ accordion, phone validation, duplicate-submission prevention, and dynamic WhatsApp message generation.
- `src/styles.css`: responsive blue/white/red/green healthcare design with mobile breakpoints and accessible focus states.
- `sitemap.xml` and `robots.txt`: crawlable search foundations.
- `public/manus-routes.json` and root `manus-routes.json`: route manifest for `/`.

## Enquiry behavior
The form is clearly labelled as an enquiry fallback. It validates required fields and Bangladeshi mobile numbers, prevents duplicate submits in the current session, and opens a prefilled WhatsApp message for the user to review and send. It never claims delivery or confirmation.
