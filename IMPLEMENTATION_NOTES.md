# Roaring Tours & Adventures — v3 development handoff

## Delivered
- Luxury tropical Next.js frontend, branded assets, mobile navigation.
- Exact approved navigation: Home, Airport Transfer, Private Taxis, Excursions (five destinations), Plan Your Trip, Contact Us.
- Jamaica Travel Guide linked in homepage and footer (not primary navigation), with three starter guides.
- Contact: +1 (876) 839-4976; Tours@roaring-adventures.com.
- Source pricing extracted into `content/pricing.json` from the supplied DOCX for CMS import and QA.
- Booking inquiry form currently opens email; no actual payment or live inventory is active.

## Must complete before accepting live bookings
1. Choose and test a booking provider that supports Jamaica-based PayPal Business accounts, group capacity and tour/driver resource availability.
2. Configure paid inventory and verified PayPal checkout; do not claim instant booking until tested.
3. Add a Sanity project, content schemas, secured API configuration, price rules and editorial workflows.
4. Confirm all prices and promotional terms against source DOCX and add Port Antonio products only after approval.
5. Import genuine Viator reviews only with appropriate permissions, attribution and source links; no fabricated ratings.
6. Verify accessibility, SEO metadata, deployment, domain DNS, and existing Nomadic | Twelve Tribes planner migration.
7. Use only licensed imagery for production. Some existing destination images are generic remote placeholders.

## Local run
`npm install` then `npm run dev`. Set up a private GitHub repository and Vercel Pro project before commercial launch. Keep Squarespace active until migration and testing complete.
