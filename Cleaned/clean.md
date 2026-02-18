#  Data Cleaning Process 

## Copying Raw Data

First, we copied the `retail_store_sales_raw` sheet into a new working
sheet.\
This was done to keep the original raw data safe and unchanged.

------------------------------------------------------------------------

## Removing Duplicates

After copying the data: - We removed all duplicate records. - This
ensured that each transaction appears only once.

------------------------------------------------------------------------

## Handling Null (Blank) Values

-   We identified blank/null values in the dataset
-   Applied filters to all columns to easily detect missing values.
-   Removed or filtered out rows containing unnecessary blank values.

To remove rows where Column D was blank, we used:

=FILTER(retail_store_sales_raw!A:J, retail_store_sales_raw!D:D\<\>"")

This removed all rows with null values in Column D and fixed Pivot Table
errors.

------------------------------------------------------------------------

## Fixing Discount Formula

We corrected the discount formula using:

=IF( XLOOKUP(A2, retail_store_sales_raw!A:A,
retail_store_sales_raw!K:K,,0), XLOOKUP(A2, retail_store_sales_raw!A:A,
retail_store_sales_raw!K:K,,0), FALSE )

This formula: - Looks up the discount value using XLOOKUP - Returns the
discount if found - Returns FALSE if no match is found

------------------------------------------------------------------------

## Numeric Formatting & Standardization

-   Applied proper numeric formatting to columns.
-   Standardized data types across the table.
-   Ensured consistency in number, currency, and date formats.

------------------------------------------------------------------------

## Extracting Date Information

From the Transaction Date column, we extracted: - Transaction Year -
Transaction Month

This helps in better time-based analysis and visualization.

------------------------------------------------------------------------

# Final Result

After completing all these steps: - The dataset is clean\
- No duplicates\
- No unnecessary null values\
- Correct formulas applied\
- Proper formatting done\
- Ready for Pivot Tables and Data Visualization

The dataset is now fully prepared for analysis in the DVA project.
