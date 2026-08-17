# Stoa Paris — Order Analyzer

A single self-contained HTML dashboard that turns Shopify `orders_export_*.csv` files into a
full customer & product analytics view — purchase cadence, LTV/RFM segments, cohort retention,
product performance, product journeys, frequently-bought-together, geography and discount impact.

Everything runs **client-side in your browser**. No data is uploaded anywhere.

## Use it

Open [`index.html`](./index.html) directly (or via GitHub Pages, if enabled for this repo),
then drop your Shopify order-export CSV files onto the page — or select the folder they're in —
and the dashboard builds itself locally in your tab.

## Notes

- Product categories are currently inferred from product titles (Bedsheet Set, Comforter, Duvet
  Cover, Quilt, Pillow Covers, Cushion Covers, Towel, Throw, Curtain, Rug, Blanket, Gift Card).
  Swap in a SKU → collection master file for an exact mapping.
- No customer data is stored in this repo — the dashboard is just the analysis tool; you supply
  the CSVs yourself each time you open it.
