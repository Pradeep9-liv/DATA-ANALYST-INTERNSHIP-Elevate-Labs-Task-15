# DATA-ANALYST-INTERNSHIP-Elevate-Labs-Task-15

# RFM Customer Segmentation – Online Retail II

## Objectives
- Load and clean raw e-commerce transaction data
- Remove canceled invoices and invalid records
- Convert invoice dates into datetime format
- Calculate RFM metrics:
  - **Recency** – Days since last purchase
  - **Frequency** – Number of unique purchases
  - **Monetary** – Total customer spending
- Create quantile-based RFM scores
- Assign customer segments
- Visualize customer distribution
- Export final segmentation results

---

## Dataset
**Dataset Used:** Online Retail II  
**Type:** E-Commerce Transactions  
**Format:** CSV  

### Key Columns
- `Invoice` – Invoice number
- `StockCode` – Product code
- `Description` – Product description
- `Quantity` – Number of items purchased
- `InvoiceDate` – Transaction date
- `Price` – Unit price
- `Customer ID` – Unique customer identifier
- `Country` – Customer location

---

## Data Cleaning Steps
1. Removed rows with missing `Customer ID`
2. Removed canceled invoices (Invoice starting with **C**)
3. Removed negative or zero quantities
4. Converted `InvoiceDate` to datetime format
5. Created `TotalPrice = Quantity × Price`

---

## RFM Calculation
Customers were grouped by **Customer ID** to compute:

- **Recency:** Days since last purchase
- **Frequency:** Number of unique invoices
- **Monetary:** Total spending

A snapshot date was defined as the latest transaction date + 1 day.

---

## RFM Scoring
Quantile-based scoring (1–4 scale):

- High Recency score → Recent customers
- High Frequency score → Frequent buyers
- High Monetary score → High spenders

Combined RFM score created for segmentation.

---

## Customer Segments
Customers were categorized into business-friendly segments:

- Champions
- Loyal Customers
- Potential Loyalists
- At Risk
- Hibernating

---

## Visualization
A bar chart was created to show the distribution of customer segments using **Matplotlib**.

---
## customer_rfm_segmentation.csv
Contains:
- Recency
- Frequency
- Monetary
- RFM Scores
- Segment Labels

---

## Business Actions (Strategy)

### Champions
- Provide VIP offers and early product access
- Encourage referrals
- Launch premium loyalty rewards

### Loyal Customers
- Cross-sell premium products
- Personalized email campaigns
- Reward repeat purchases

### Potential Loyalists
- Offer limited-time discounts
- Promote second purchases
- Targeted onboarding campaigns

### At Risk
- Send win-back campaigns
- Offer personalized incentives
- Collect feedback surveys

### Hibernating
- Low-cost reactivation emails
- Seasonal promotions
- Reduce marketing spend if inactive

---

## Tech Stack
- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

---

## Key Skills Demonstrated
- Data Cleaning & Preprocessing
- Feature Engineering
- Customer Analytics
- RFM Modeling
- Data Visualization
- Business Insight Generation

---

## Conclusion
This project demonstrates how transactional data can be transformed into actionable customer segments using RFM analysis.  
The segmentation helps businesses improve marketing efficiency, increase retention, and drive revenue growth.
