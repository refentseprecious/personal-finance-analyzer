 Personal Finance Analyzer

A Python data pipeline that ingests transaction data, categorizes spending, summarizes trends, and automatically detects recurring subscriptions.

 What it does

1. Ingest — Reads transaction records (date, merchant, amount) into a pandas DataFrame.
2. Categorize — Maps each merchant to a spending category (e.g. Coffee, Groceries, Subscription, Transport) using a merchant-to-category lookup.
3. Summarize — Aggregates total spending per category to reveal where money goes.
4. Visualize — Renders a bar chart of spending by category using matplotlib.
5. Detect recurring subscriptions — Flags merchants that appear 3+ times with a consistent charge amount (low variance relative to the average), catching subscriptions like Netflix, Spotify, or gym memberships automatically.

Tech stack

- Python
- pandas — data manipulation and aggregation
- numpy — data generation and numerical operations
- matplotlib — visualization

Current status

Currently runs on generated sample data to validate the pipeline end-to-end. Designed to be extended to real bank statement exports — swap the data-loading step for `pd.read_csv()` on a real statement, and update the category mapping to match real merchant names.

 Possible next steps

- Load real bank CSV exports instead of sample data
- Add month-over-month trend analysis
- Flag anomalous/unusually large transactions
- Turn merchant-to-category mapping into a small ML text classifier for unseen merchants

