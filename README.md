# 2022-income-and-inflation

The goal of this project is to explore the effects of inflation on people in different income groups. 

## Hypothesis

While higher-income households bear a larger inflationary burden compared with lower-income households in terms of absolute dollar amounts, taking income into account shows inflation hits lower-income households a lot harder. That's because inflation costs take up a larger proportion of the income of lower-income households.


## Data sources

This project uses two U.S. Bureau of Labor Statistics (BLS) data sets:
- [Consumer Price Index (CPI), Western Region – July 2022](hhttps://www.bls.gov/regions/west/news-release/consumerpriceindex_west.htm)
    - The CPI report is published monthly and provides the inflation rate for expenditure categories for specific regions. This is the source for how prices are rising for different types of goods and services.
    - This analysis uses the Western Region, which includes Oregon. The West Region  includes Alaska, Arizona, California, Colorado, Hawaii, Idaho, Montana, Nevada, New Mexico, Oregon, Utah, Washington and Wyoming.
- [Table 3104. Western region by income before taxes: Average annual expenditures and characteristics, Consumer Expenditure Surveys (CES), 2019-2020](https://www.bls.gov/cex/tables/cross-tab/mean/cu-region-by-income-west-2020.pdf)
    - The CES report is published annually and provides data on expenditures and incomes for households of different income groups. This is the source for the breakdown of how different income groups spend their money across various categories.

## Some notes regarding the data
1. This analysis uses data from two income groups:
      - The low-income households are those that earn between $15,000 and $30,000.
      - High-income households earn between $100,000 and $149,999.

2. The `housing` category refers to `shelter` expenditures, which describe rent or mortgage payments and accounts for how high-income households usually hold property and low-income households usually rent. The analysis excludes some data in the BLS `housing` expenditures category, which includes utilities and other housing-related expenditures. 

2. The `transportation` category includes the costs of buying fuel, paying for public transportation, and purchasing new and used vehicles. `Gas` costs fall into the fuels subcategory of transportation and are distinct from the natural gas costs used in household contexts like heat and cooking, which are counted as utilities within housing expenditures.

3. The expenditure categories in the CPI and CES data have different names. Calculating the inflation costs required matching categories that may not perfectly align, and in some cases meant using subcategories to be as aligned as possible. But here's how the categories are lined up:

| Consumer Price Index      | Consumer Expenditure Survey |
| ----------- | ----------- |
| Food at home      | Food at home       |
| Food away from home	   | Food away from home	        |
| Alcoholic beverages     | Alcoholic beverages       |
| Shelter	   | Shelter	        |
| Household furnishings and operations      | Household operations + Housekeeping supplies +  Household furnishings and equipment       |
| Fuels and utilities	   | Utilities, fuels, and public services	        |
| Apparel      | Apparel and services       |
| Motor fuel   | Gasoline, other fuels, and motor oil	        |
| Medical care	   | Healthcare	        |
| Recreation	   | Entertainment	        |
| Education and communication	   | Education	        |
| Other goods and services	   | Personal care products and services + Reading + Tobacco products and smoking supplies + Miscellaneous + Cash contributions + Personal insurance and pensions	        |
