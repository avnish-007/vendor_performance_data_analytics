# Vendor Performance Data Analytics

Data analytics project analyzing vendor (supplier) performance for a liquor/beverage distribution business across multiple stores for **calendar year 2024**.

## Datasets

The raw CSV datasets are not tracked in Git due to size (~2 GB total). Place them in the `datasets/` folder:

| File | Description |
|---|---|
| `sales.csv` (~1.5 GB) | Daily sales transactions by store, brand, and vendor |
| `purchases.csv` (~345 MB) | Purchase orders with vendor, PO, and receiving details |
| `begin_inventory.csv` (~17 MB) | Opening inventory (2024-01-01) by store and brand |
| `end_inventory.csv` (~19 MB) | Closing inventory (2024-12-31) by store and brand |
| `vendor_sales_summary.csv` (~2 MB) | Pre-aggregated vendor-level profit and turnover metrics |
| `purchase_prices.csv` (~1 MB) | Brand-level pricing and vendor mapping |
| `vendor_invoice.csv` (~500 KB) | Vendor invoices with freight and payment details |

## Setup

1. Install dependencies:
   ```bash
   pip install pandas sqlalchemy psycopg2-binary
   ```
2. Create a PostgreSQL database named `vendor_performance_data`.
3. Place CSV files in `datasets/` and run `datasets/load_data_to_postgres.ipynb` to load data.
4. Open `vendor_performance_data_analytics.ipynb` for analysis.

## Tech Stack

- Python 3.13 · Pandas · SQLAlchemy · PostgreSQL
