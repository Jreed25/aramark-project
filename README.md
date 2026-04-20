# Aramark–Avendra Spend Analysis
**CS 562 — Big Data Algorithms | Rutgers University**

## Project Overview
This project analyzes Aramark–Avendra's supply chain purchasing dataset to generate insights for two distinct audiences:
- **Client / Leadership** (CFO, Regional VP) — portfolio-level, strategic, benchmarking
- **Customer / On-Site Operator** (GM, Chef, Dining Director) — daily tactical, cost control, peer comparison

---

## Team Members
- [Name 1]
- [Name 2]
- [Name 3]
- [Name 4]

---

## Setup Instructions

### Requirements
- A `@scarletmail.rutgers.edu` Google account (required for GCS data access)
- A Google account to use Google Colab (free)

### How to Run the Notebook

1. **Clone this repository**
   ```bash
   git clone https://github.com/your-repo-link
   ```

2. **Open the notebook in Google Colab**
   - Go to [colab.research.google.com](https://colab.research.google.com)
   - Click **File → Open Notebook → GitHub**
   - Paste the repository URL and select `eda_colab.ipynb`

   Or click the badge below:

   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-repo-link/blob/main/eda_colab.ipynb)

3. **Run the first cell — Authenticate**
   - It will pop up a Google login
   - Sign in with your `@scarletmail.rutgers.edu` account
   - This grants access to the GCS bucket

4. **Run all remaining cells in order**
   - The data load cell will take **10–20 minutes** (8.5GB file)
   - Do not interrupt it

---

## Saving Your Work Back to GitHub

After making changes in Colab:
1. **File → Save a copy in GitHub**
2. Select the correct repo and branch
3. Write a commit message and click **OK**

---

## Repository Structure
```
aramark-project/
│
├── eda_colab.ipynb         # Main EDA notebook (run in Google Colab)
├── requirements.txt        # Python dependencies (for local use)
├── .gitignore              # Files excluded from version control
└── README.md               # This file
```

---

## Data Access
The dataset is stored in a private Google Cloud Storage bucket:
```
gs://cs-562-aramark-project/Andrew_Meszaros_SRF_2026-04-01-0936.csv
```
- Access requires a Rutgers scarletmail account authorized by the professor
- The data is **proprietary and anonymized** — do not share or redistribute
- **You must delete any locally downloaded copies at the end of the course**

### Data Dictionary
| Column | Type | Description |
|--------|------|-------------|
| Year Name | Text | Calendar year of spend record |
| Year Month | Text | Calendar year and month (e.g. 2025-01) |
| Business Entity Type | Text | Customer business type (Hotel, Restaurant, etc.) |
| Country | Text | Customer country (US only) |
| Customer Market Segment Id | Text | Market segment identifier |
| Client ID | Text | Top-level parent account identifier |
| Customer Id | Text | Individual customer location identifier |
| Customer Brand Id | Text | Brand identifier |
| Customer Brand Parent Id | Text | Parent brand identifier |
| City | Text | Customer city |
| State | Text | Customer US state abbreviation |
| Zip | Text | Customer ZIP code |
| Number of Rooms | Number | Rooms at property (hospitality only) |
| Ecommerce Status | Text | Ecommerce platform status (Active/Inactive) |
| Distributor ID | Text | Fulfilling distributor identifier |
| Distributor Group | Text | Distributor group classification |
| Manufacturer ID | Text | Product manufacturer identifier |
| Category ID | Text | Granular product category code |
| Category Level 1 | Text | Top-level category (Food, Beverage, etc.) |
| Category Level 2 | Text | Second-level category |
| Category Level 3 | Text | Third-level category |
| Category Level 4 | Text | Most granular category |
| Spend Random Factor | Number (USD) | Randomized total spend in USD |

---

## Analysis Directions
- Customer segmentation (clustering)
- Spend prediction (machine learning)
- Association rule mining (frequent itemsets)

---

## Professor
- **GitHub:** [@sshende](https://github.com/sshende) — add as collaborator to the private repo
