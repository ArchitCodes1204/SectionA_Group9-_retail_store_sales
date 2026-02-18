
## Pivot Analysis Documentation

---

## Project Objective

This project analyzes retail transaction data to evaluate revenue performance, store contribution, product drivers, and performance trends.

The key business question addressed is:

> Which stores and product categories contribute most to revenue, and what performance trends support better strategic decision-making?

The pivot tables were designed to convert raw transaction-level data into structured business insights.

---

## Why These Columns Were Selected

### Transaction Date
Used for:
- Monthly revenue trend
- Growth rate analysis
- Seasonality detection
- Revenue stability measurement

Business Use:
Helps management understand whether the business is growing, declining, or fluctuating over time.

---

### Total Spent
Primary revenue metric.

Used to calculate:
- Total Revenue
- Contribution %
- Growth %
- Volatility
- Revenue Concentration Ratio

Business Use:
Represents overall financial performance of the company.

---

### Transaction ID
Used to calculate:
- Total Transactions
- Average Order Value (AOV)

Business Use:
Measures sales activity and customer engagement.

---

### Quantity
Used for:
- Units sold
- Volume vs revenue comparison

Business Use:
Helps identify whether revenue is driven by high demand or high pricing.

---

### Location (Store Type)
Used to evaluate:
- Store revenue contribution
- Channel performance
- Revenue concentration risk

Business Use:
Identifies which channel contributes most revenue and whether the business is dependent on one channel.

---

### Category
Used for:
- Product contribution analysis
- Revenue driver identification

Business Use:
Supports inventory planning and marketing strategy.

---

### Discount Applied
Used for:
- Promotion impact analysis

Business Use:
Evaluates effectiveness of discount strategies.

---

### Payment Method
Used to analyze:
- Revenue distribution by payment type

Business Use:
Provides insight into customer payment behavior and digital adoption.

---

## Pivot Tables and Business Logic

### 1. Monthly Revenue Trend Pivot

Rows:
- Transaction Date (Year-Month)

Values:
- SUM of Total Spent
- COUNTA of Transaction ID
- SUM of Quantity

Additional Calculations:
- MoM Growth %
- Monthly Moving Average
- Sales Volatility Index

Business Use:
- Tracks revenue trends
- Identifies growth patterns
- Measures performance stability
- Supports forecasting

---

### 2. Store Performance Pivot

Rows:
- Location

Values:
- SUM of Total Spent
- % of Grand Total
- Transaction Count

Business Use:
- Identifies revenue contribution by store
- Compares channel performance
- Evaluates revenue concentration risk

---

### 3. Category Performance Pivot

Rows:
- Category

Values:
- SUM of Total Spent
- SUM of Quantity
- % of Grand Total

Business Use:
- Identifies revenue-driving categories
- Supports product-level strategy
- Guides marketing focus

---

### 4. Store Growth Over Time Pivot

Rows:
- Year-Month

Columns:
- Location

Values:
- SUM of Total Spent

Business Use:
- Compares growth trends across stores
- Identifies stable vs declining channels

---

### 5. Discount Impact Pivot

Rows:
- Discount Applied

Values:
- SUM of Total Spent
- % of Grand Total
- Transaction Count

Business Use:
- Measures promotional impact on revenue

---

### 6. Payment Method Share Pivot

Rows:
- Payment Method

Values:
- SUM of Total Spent
- % of Grand Total
- Transaction Count

Business Use:
- Identifies dominant payment modes
- Supports digital payment strategy

---

## Key KPIs and Strategic Importance

Revenue Growth Rate (%)
- Measures month-over-month revenue change
- Indicates business momentum

Monthly Moving Average
- Smooths short-term fluctuations
- Reveals long-term trend

Sales Volatility Index
- Measures revenue stability
- Indicates performance risk

Revenue Concentration Ratio
- Top store revenue ÷ total revenue
- Identifies dependency risk

---

## Conclusion

The pivot analysis transforms raw transaction data into actionable business intelligence.

It enables:

- Revenue driver identification
- Store performance evaluation
- Trend monitoring
- Stability assessment
- Risk analysis
- Data-driven strategic decision-making

