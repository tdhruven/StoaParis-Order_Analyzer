# Stoa Paris — Order Analyzer

A single self-contained HTML dashboard that turns Shopify `orders_export_*.csv` files into a
full customer & product analytics view — purchase cadence, LTV/RFM segments, cohort retention,
product performance, collections, sizes, category/collection cross-sell, product journeys,
frequently-bought-together, geography and discount impact. Responsive down to phone width.

Everything runs **client-side in your browser**. No data is uploaded anywhere.

## Use it

Open [`index.html`](./index.html) directly (or via GitHub Pages, if enabled for this repo),
then drop your Shopify order-export CSV files onto the page — or select the folder they're in —
and the dashboard builds itself locally in your tab.

## SKU master file

`Category`, `Collection` and `Size` are read straight from a SKU master file baked into the
page as `MASTER_SKU_MAP` (Product Code → category/collection/size/fabric/etc.), so every
rollup, filter and product table reflects your real merchandising taxonomy instead of a
guess from the product title. Line items whose SKU isn't found there fall back to a
name-based guess (shown as "Unmapped" in the Collection view) so nothing is dropped.

To refresh it after a catalog change, re-export the master spreadsheet and regenerate
`MASTER_SKU_MAP` (Product Code, with warehouse suffixes like `_BOM`/`_BLR`/`_DEL` and
trailing `PACK` stripped, as the key) — nothing else in the dashboard needs to change.

## Notes

- No customer data is stored in this repo — the dashboard is just the analysis tool; you supply
  the CSVs yourself each time you open it.
