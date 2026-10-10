# Real Estate Data Cleaning Pipeline

An end-to-end data cleaning and transformation pipeline built with Python and Pandas to clean messy residential property listings.

## Tech Stack
- Python 3.11+
- Pandas, NumPy
- Jupyter Notebook

## Cleaning Highlights
- **Deduplication:** Purged 1,237 duplicate records.
- **Unit Standardisation:** Converted non-uniform land metrics (Kanal/Marla) into unified numerical `Area_Marla`.
- **Currency Normalisation:** Parsed Pakistani Rupee textual denominations (Crore / Lakh) into pure numeric `Price_PKR`.
- **Missing Value Strategy:** Handled placeholder strings (`'-'`) with robust median imputation.
- **Outlier Treatment:** Applied IQR capping to preserve row volume while removing statistical skew.

## How to Run
1. Clone the repository:
   ```bash
   ```bash
git clone [https://github.com/](https://github.com/)<your-username>/data-cleaning-portfolio.git
cd data-cleaning-portfoliolio
