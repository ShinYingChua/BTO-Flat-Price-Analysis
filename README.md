## 1. Overview of the folder structure
    .
    ├── eda.ipynb                                   
    ├── price-range-of-hdb-flats-offered.csv                    
    └── README.md
    
## 2. Extract
The data is extracted from Data.gov.sg and is based on Singapore, ranging over FY2008-2021. The financial year starts on 1 Apr and ends on 31 Mar.

## 3. Transform
1) Columns "min_selling_price_less_ahg_shg" and "max_selling_price_less_ahg_shg" are dropped as the information is not useful.
2) There is presence of row with zeros values( $0 min/max selling price) and these rows are dropped.

## 4. Load
- Created database and respective tables to match the columns from dataframe using sql
<img width="396" alt="image" src="https://github.com/ShinYingChua/Construction-Material-and-BTO-Price/assets/101923627/25923926-5e9a-4a6d-b807-a3fb99897454">
- Connect to mySQL database using mysql.connector 
- Load data into database
## 5. SQL Query
<img width="577" alt="image" src="https://github.com/ShinYingChua/Construction-Material-and-BTO-Price/assets/101923627/185b0ec2-083a-4e60-a381-c0ca3de1be09">

## Key Findings from EDA
-  General increase in selling price of BTO flats between FY2008-2021
-  As the BTO flats size increases, the selling price increases
<img width="1236" alt="image" src="https://github.com/ShinYingChua/Construction-Material-and-BTO-Price/assets/101923627/a3ae43b5-ba96-482b-8358-a7ef05449d26">
<img width="1236" alt="image" src="https://github.com/ShinYingChua/Construction-Material-and-BTO-Price/assets/101923627/4a04c04b-03e7-4c4e-a553-2ab8c7e4c59b">

-  Between FY2008-2019, the selling price of BTO flats in Punggol is generaally the highest for all room types
<img width="1238" alt="image" src="https://github.com/ShinYingChua/Construction-Material-and-BTO-Price/assets/101923627/201c1712-afe9-498f-9b87-60fcfd0ce7cd">
<img width="1238" alt="image" src="https://github.com/ShinYingChua/Construction-Material-and-BTO-Price/assets/101923627/fdd51be8-8d37-4a8f-9863-8b796e19a560">

