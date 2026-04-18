EXPERIMENT 14 : Data Binning and Data Formatting using Python**

*AIM*: **To perform **data binning** and **data formatting** using Python libraries like **Pandas** and **NumPy**, and analyze structured datasets effectively** 

*THEORY*:

Data Binning
Data binning is the process of **grouping continuous data into categories (bins)**. It helps in:
- Simplifying large datasets  
- Improving data analysis  
- Identifying patterns  

Example: Converting numerical values into categories like *Low*, *Medium*, and *High*.

---

Data Formatting
Data formatting involves **modifying data types and structure** to make it consistent and usable.

It includes:
- Changing data types (int → float)  
- Formatting text (uppercase/lowercase)  
- Rounding numerical values  

---
pd.DataFrame(): Creates a structured table (DataFrame) from dictionary or data.

print(): Displays output on the console.

pd.cut(): Divides continuous data into discrete bins or categories.

bins: Defines the range intervals for categorization.

labels: Assigns names to each bin category.

df['new_column'] = pd.cut(): Creates a new categorical column based on binning.

df.dtypes: Shows the datatype of each column in the DataFrame.

astype(): Converts data from one datatype to another.

df['col'].astype(float): Converts column values into float datatype.

df['col'].str.upper(): Converts all string values in a column to uppercase.

round(): Rounds numeric values to a specified number of decimal places.

df.sort_values(): Sorts the DataFrame based on a column.

ascending=False: Sorts data in descending (high to low) order.

ascending=True (default): Sorts data in ascending (low to high) order.

df['col'].unique(): Returns unique values from a column.

value_counts(): Counts frequency of each category in a column.

Multiple binning: Applying pd.cut() on different columns to categorize different features.

Categorical Data Analysis: Helps in grouping continuous data into meaningful ranges for interpretation.


##  Libraries Used
- **Pandas** → Data manipulation and analysis  
- **NumPy** → Numerical operations  


### Data Binning using `pd.cut()`
Data binning is performed using the `cut()` function from Pandas.  
This function divides continuous numerical data into discrete intervals (bins).

- The `bins` parameter defines the range of values.
- The `labels` parameter assigns category names to each bin.

This helps in converting raw numerical values into meaningful categories such as *Low*, *Medium*, and *High*, making analysis more intuitive.

### Creating New Columns
New columns such as `Price_Category` and `Sales_Category` are created to store the categorized data.  
This enhances the dataset by adding derived information without modifying the original data.

### Data Type Conversion using `astype()`
The `astype()` function is used to convert data types.

Example:
- Integer values are converted into float type for consistency and better numerical operations.

This ensures uniformity in the dataset and prevents errors during calculations.


### Text Formatting using String Functions
String operations such as `.str.upper()` are applied to modify text data.

- Converts all text values into uppercase.
- Helps maintain consistency in categorical data.

### Rounding Values using `round()`
The `round()` function is used to limit decimal places in numerical values.

- Improves readability of data
- Useful when dealing with financial or precise datasets


### Sorting Data using `sort_values()`
Sorting is performed using the `sort_values()` function.

- Arranges data in ascending or descending order
- Helps in identifying trends such as highest or lowest values

### Finding Unique Values using `unique()`
The `unique()` function returns all distinct values from a column.

- Helps in understanding the variety of categories present
- Useful for quick data inspection

### Frequency Counting using `value_counts()`
The `value_counts()` function counts occurrences of each category.

- Provides distribution of data
- Helps in statistical analysis and decision making

## Second Dataset Theory (Food Delivery)

### Multi-Feature Binning
Multiple columns such as:
- Order Value  
- Delivery Time  
- Distance  

are categorized using binning techniques.

This allows comparison and analysis across different dimensions of the dataset.


### Data Formatting in Second Dataset
- Conversion of delivery time into float ensures consistency  
- Text formatting standardizes category labels  
- Sorting improves data readability and interpretation  

### Data Analysis Enhancement
By combining:
- Binning  
- Formatting  
- Sorting  
- Counting  

the dataset becomes more structured and easier to analyze, enabling better insights into patterns and trends.

*CONCLUSION:*

Successfully performed data binning to convert continuous values into meaningful categories.
Applied data formatting techniques such as type conversion, text transformation, and rounding.
Used sorting and aggregation functions to enhance data analysis.
Demonstrated how structured data can be easily analyzed using Pandas.
Improved understanding of real-world datasets like product sales and food delivery systems.
