# Direct booking setup — Roaring Tours & Adventures

## Recommended launch architecture
- Next.js hosts the marketing website and the `/book` route.
- TidyCal Free provides **provider-managed calendar availability** and PayPal checkout for eligible fixed-price excursions.
- Existing Jamaica-registered PayPal Business account receives payments, subject to successful integration and real test transaction.
- Custom excursions, airport transfers and private taxis use manual quotes until their pricing/capacity rules are verified.

## Setup
1. Create a TidyCal account and connect a calendar that reflects all actual vehicle/guide commitments.
2. In TidyCal > Integrations > Payments, add the business PayPal email. Test with the existing Jamaica business account.
3. Create paid booking types for confirmed fixed-price excursions (including the Negril Kayak Photoshoot). Configure durations, buffers, group limits, time zone `America/Jamaica`, availability, and refund policy.
4. Verify whether group bookings, required guest information, booking questions, and simultaneous inventory are supported on the chosen tier. Do not offer instant bookings for products without validated capacity controls.
5. Copy the public booking-page URL into `NEXT_PUBLIC_TIDYCAL_BOOKING_URL` on Vercel and redeploy. The `/book` page embeds that URL. If provider embedding is restricted, the fallback opens the booking page separately.
6. Test from a phone and desktop with a real low-value purchase, PayPal payment receipt, booking confirmation, cancellation, and refund.
7. Configure email delivery and policies before launch. Keep your current Squarespace site active until verified.

## Important limitations
This integration is **not yet activated**; no PayPal account or calendar credentials have been connected. TidyCal's availability is based on its calendar configuration and does not automatically represent taxi fleet capacity, excursion suppliers, or overlapping vehicle bookings. The `/book` route is a working integration shell, not a verified production booking flow. Payment occurs on the provider's checkout, not directly within custom code.

## Cost notes (verified November 2026)
TidyCal Free: $0 subscription, PayPal payments supported, with standard PayPal merchant fees. TidyCal's 1% platform fee applies to Stripe transactions, not PayPal. TidyCal Individual Lifetime: advertised $29 one-time and includes additional group-booking features. Verify current terms and Jamaica PayPal compatibility before buying.
Sources: https://tidycal.com/pricing and https://help.tidycal.com/article/149-connecting-payment-services
