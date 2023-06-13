## 1. Overview of the folder structure
    .
    ├── ETL.ipynb                                   
    ├── README.md                
    └── price-range-of-hdb-flats-offered.csv    
    
## 2. Extract
The data is extracted from Data.gov.sg and is based on Singapore, ranging over FY2008-2021. The financial year starts on 1 Apr and ends on 31 Mar.

## 3. Transform
1) Columns "min_selling_price_less_ahg_shg" and "max_selling_price_less_ahg_shg" are dropped as the information is not useful.
2) There is presence of row with zeros values( $0 min/max selling price) and these rows are dropped.

## 4. Load
- Created database and respective tables to match the columns from dataframe using sql
<img width="592" alt="image" src="https://github.com/ShinYingChua/BTO-Flat-Price-Analysis/assets/101923627/59732e6b-3eb3-4e71-ac5f-cc2b373e3548">

- Connect to mySQL database using mysql.connector 
- Load data into database
## 5. SQL Query
<img width="592" alt="image" src="https://github.com/ShinYingChua/BTO-Flat-Price-Analysis/assets/101923627/b55baf57-49fd-46ee-bba4-fd8c2918c1b0">
<img width="592" alt="image" src="https://github.com/ShinYingChua/BTO-Flat-Price-Analysis/assets/101923627/f8d5a9e0-c941-4f57-b8f7-d652b9161899">

## Key Findings from EDA
-  General increase in selling price of BTO flats between FY2008-2021
-  As the BTO flats size increases, the selling price increases
<img width="1241" alt="image" src="https://github.com/ShinYingChua/BTO-Flat-Price-Analysis/assets/101923627/2a8a68c6-ddae-48f7-82b3-58569fe0af8e">
<img width="1241" alt="image" src="https://github.com/ShinYingChua/BTO-Flat-Price-Analysis/assets/101923627/6744d5d6-4687-411f-9f62-98d78ebf4d0d">

-  Between FY2008-2019, the selling price of BTO flats in Punggol is generaally the highest for all room types
<img width="1241" alt="image" src="https://github.com/ShinYingChua/BTO-Flat-Price-Analysis/assets/101923627/d89cac27-01b1-45ce-b462-d9f7aa0276c7">
<img width="1241" alt="image" src="https://github.com/ShinYingChua/BTO-Flat-Price-Analysis/assets/101923627/a5cc647e-da37-4f5e-aad5-61e10b382191">


