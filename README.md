# Coastal Solar Solutions: Google Ads landing pages

Four ad-group landing pages plus a thank-you page. Built by NetWorth Digital.
Design DNA matched to coastalsolarsolutions.com.au.

| Ad group | Path |
|---|---|
| Coastal Solar AD SET | `/` |
| Solar System Cost | `/solar-system-cost/` |
| EV Charger Installation | `/ev-charger-installation/` |
| Battery & NSW Rebate | `/battery-rebate-nsw/` |
| Thank you (conversion trigger) | `/thank-you/` |

## Quote form
LeadConnector inline embed, form ID `kLBCl7AnenhFvoYT0Etn`. Renders in the hero
on desktop and in the quote section on mobile.

## Tracking
- GHL external tracking: `tk_c30e8f109f3b41e4b0a06d918ae654d5`, in every head.
- Google Ads: fill `window.CSA` at the top of each page with `AW_ID`,
  `LEAD_LABEL` and `CALL_LABEL`. Until `AW_ID` is set, nothing loads.
  Lead fires on `/thank-you/` load and on the LeadConnector submit message,
  deduped via sessionStorage. Call fires on any `tel:` click.
- Set the GHL form's on-submit redirect to `/thank-you/` for reliable firing.

## Before go-live
Remove the `noindex` meta tag only if you want these indexed. Google Ads does
not require indexable pages, so leaving noindex on is fine and avoids
duplicate-content overlap with the main site.
