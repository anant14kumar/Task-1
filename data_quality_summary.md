# Data Quality & Cleaning Audit Report

## Dataset Overview
- **Domain:** Real Estate (Housing Data)
- **Raw Observations:** 7,500 rows | 16 columns
- **Clean Observations:** 6,263 rows | 16 columns

## Issues Identified & Rectifications
1. **Duplicates:** 1,237 identical rows detect hui aur data distribution ko normalise karne ke liye unhe drop kiya gaya.
2. **Hidden Nulls in 'Baths' & 'Beds':** Data mein missing values `'-'` ke roop mein thi, jinhe numeric cast karke column-wise median se impute kiya gaya.
3. **Inconsistent Price Formatting:** String values jaise `'PKR 3.5 Crore'` aur `'PKR 85 Lakh'` ko actual PKR currency numbers (Float) mein calculate karke standardise kiya gaya.
4. **Mixed Measurement Units:** Property areas `Marla` aur `Kanal` mein mixed the. Mathematical conversion rule ($1\text{ Kanal} = 20\text{ Marla}$) ke zariye pure column ko standard `Marla` float mein convert kiya gaya.
5. **Outliers (IQR Capping):** Store rooms (up to 32) aur Kitchens (up to 20) mein extreme values the, jinhe 1.5 * IQR standard se cap/winsorize kiya gaya taaki data loss na ho.
