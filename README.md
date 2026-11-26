### 🇩🇪 Du reist aus Deutschland in die Türkei und suchst eine günstige eSIM?

Es gibt zahlreiche eSIM-Anbieter mit unterschiedlichen Preisen, Datenpaketen und Mobilfunknetzen. Doch welche eSIM bietet wirklich das beste Preis-Leistungs-Verhältnis für deine Türkei-Reise?

Wir helfen dir, den Überblick zu behalten! Vergleiche verschiedene eSIM-Anbieter, aktuelle Preise, Datenvolumen, Laufzeiten und verfügbare Mobilfunknetze – alles an einem Ort.

Finde die passende Türkei-eSIM für dein Reisebudget und vermeide unnötige Kosten für mobiles Internet.

**Jetzt Türkei-eSIMs vergleichen und den besten Tarif finden:**

👉 https://e-simturkei.de

👉 **Alle Türkei-eSIM-Tarife vergleichen:** https://www.e-simturkei.de/vergleich

👉 **Den besten Türkei-eSIM-Tarif berechnen:** https://www.e-simturkei.de/esim-turkei-rechner




# eSIM-Turkei
A simple Next.js Turkey eSIM price calculator that helps travellers find the cheapest eSIM plans based on their data requirements and trip duration.



# Turkey eSIM Calculator

A simple Next.js app that helps visitors compare Turkey eSIM plans. Users choose their data requirement, trip duration and (optionally) a preferred network. Matching plans are sorted by price, lowest first.

## Features

- Choose a data allowance from 1 GB to 50 GB.
- Set trip duration from 1 to 30 days.
- Optionally include unlimited data plans.
- Filter by mobile network.
- Sort matching plans by price.
- Provider/affiliate links on each plan.
- Plan information is loaded from a CSV file. No database is required.

## Requirements

- Node.js 20.9 or newer
- npm

## Run locally

1. Download and extract this project.
2. Open a terminal in the project folder.
3. Install dependencies:

   ```bash
   npm install
   ```

4. Start the development server:

   ```bash
   npm run dev
   ```

5. Visit http://localhost:3000

## Updating the plans

Edit:

```text
data/turkey-esim-plans.csv
```

The first line contains the column names. Keep the same column names when adding or editing plans.

| Column | Meaning |
|---|---|
| `provider` | Provider name |
| `plan_name` | Name of the eSIM plan |
| `data_gb` | Included data in GB (used for fixed-data plans) |
| `validity_days` | Number of days the plan remains valid |
| `price_eur` | Plan price in EUR |
| `network` | Network used in Turkey |
| `hotspot` | Whether hotspot/tethering is supported |
| `unlimited` | `true` for unlimited plans, otherwise `false` |
| `affiliate_url` | Provider or affiliate link |
| `last_updated` | Date the price/details were checked |

Example row:

```csv
ExampleTel,Turkey 10GB,10,15,10.99,Turkcell,Yes,false,https://example.com,2026-11-26
```

### Important data notes

- Use a numeric value for `data_gb`. For unlimited plans, use a large placeholder such as `999` and set `unlimited` to `true`. The app labels those plans as “Unlimited data” and does not compare their GB value.
- Prices must be numeric and use a dot for decimals (for example `12.99`), without a currency symbol.
- If a plan has no affiliate URL, leave that field empty.
- Do not use commas inside a field unless you quote that CSV field.
- The app only shows plans that meet or exceed the requested data allowance and validity duration.
- Unlimited plans appear only when the visitor checks “Include unlimited data plans”. They are not treated as an exact data-equivalent to fixed-data plans.

## Before publishing

The included CSV contains clearly labelled sample/demo plan data and example.com links. Replace these with current, verified provider prices, plan details and your actual affiliate links before making the calculator public. Prices, validity, networks, hotspot support and fair-use terms can change; verify them with each provider and update `last_updated`.
