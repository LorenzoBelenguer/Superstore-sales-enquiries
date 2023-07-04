# Superstore-sales-enquiries
Working with the database of Superstore to answer enquiries about customers, products and sales
Exploratory Data Analysis (EDA) project 04.07.23

LINK to Google Colab full script:

https://colab.research.google.com/drive/1MPsdF2EnEU7NuMDX9RxFnmz5_tNz6PFt?usp=sharing


• Open the given script to start importing your dataset file using Google Colab
(The dataset contains information about products that has been sold from 2014 to 2017 and their customers info from a superstore in the US).


• Use the Pandas library to perform the 3 essential steps of any EDA using the
file named Superstore_dataset.csv:


1-Data Exploration:
-Explore the variables in Excel (use colouring or a whiteboard to identify and group the variables)

It's a sales data in a superstore classifying type of customer and products and whether they got a discount or not. 

-Import your file using the python pandas library and explore the file with key exploration commands

(once date transformed into date format, the rest is fine)

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 9982 entries, 0 to 9981
Data columns (total 21 columns):
 #   Column         Non-Null Count  Dtype         
---  ------         --------------  -----         
 0   Row ID         9982 non-null   int64         
 1   Order ID       9982 non-null   object        
 2   Order Date     9982 non-null   datetime64[ns]
 3   Ship Date      9982 non-null   object        
 4   Ship Mode      9982 non-null   object        
 5   Customer ID    9982 non-null   object        
 6   Customer Name  9982 non-null   object        
 7   Segment        9982 non-null   object        
 8   Country        9982 non-null   object        
 9   City           9982 non-null   object        
 10  State          9982 non-null   object        
 11  Postal Code    9982 non-null   int64         
 12  Region         9982 non-null   object        
 13  Product ID     9982 non-null   object        
 14  Category       9982 non-null   object        
 15  Sub-Category   9982 non-null   object        
 16  Product Name   9982 non-null   object        
 17  Sales          9982 non-null   float64       
 18  Quantity       9982 non-null   int64         
 19  Discount       9982 non-null   float64       
 20  Profit         9982 non-null   float64       
dtypes: datetime64[ns](1), float64(3), int64(3), object(14)
memory usage: 1.6+ MB


2-Data Cleaning:


-Remove any rows that have missing values from columns that would be an issue to identify (such as name of a customer, name of a product etc). Replace missing values by zero/mean if justified (give your reasons), remove outliers if necessary.

1. Sales and profit transformed to simple numbers to avoid future problems in python (i.e. $ and comma removed)
2. Additional spaces trimmed
3. No duplicates were found
4. Changed format to date format
5. Empty cells only found in Sub-category. “Not given value”added as it's not that relevant.
6. 12 empty cells found in Sales. Removed as unable to know.

Additional comments are in the Google Colab script

3-Data Analysis

Answers the following questions (choose an appropriate graph to answer questions):

-How many categories and sub-categories of products there are?

Categories (3)

Office Supplies    6017
Furniture          2119
Technology         1846
Name: Category, dtype: int64

Sub-categories (17)

Binders        1520
Paper          1368
Furnishings     954
Phones          889
Storage         842
Art             794
Accessories     774
Chairs          617
Appliances      466
Labels          363
Tables          319
Envelopes       253
Bookcases       228
Fasteners       217
Supplies        189
Machines        115
Copiers          68
Not given         6
Name: Sub-Category, dtype: int64

-Which products were sold the most and the least?

From the date retrieved above we can see that the product most sold were 

Binders

and the least sold were

Copiers


-Which products were sold the most in each category and sub-category?

Most sold in category product = Office supplies
Most sold in sub-category product = Binders

-Which products were sold the most in the different US regions?

Bookcases and phones seems to be the most sold. Please see 

![1stPlot](https://github.com/LorenzoBelenguer/Superstore-sales-enquiries/assets/82720058/c2b0019d-b7ce-4ada-b224-89d6abcf9250)


-Which States sold the most?

California = 1997

![which states sold the most](https://github.com/LorenzoBelenguer/Superstore-sales-enquiries/assets/82720058/0115a17f-6118-4df0-bc27-806bbfde6093)















-How many products were sold each year?

![How many products were sold each year](https://github.com/LorenzoBelenguer/Superstore-sales-enquiries/assets/82720058/85b0ed6d-6757-44fe-8c2b-1fc6f9560dfb)


-Which products were the most successful each year?

  year     Sub-Category
0  2014  (2014, Binders)
1  2015  (2015, Binders)
2  2016  (2016, Binders)
3  2017  (2017, Binders)
4  2018  (2018, Binders)

-Which customer ordered the most and what was the total value of their purchases?


                  sum  count
Customer Name                 
Sean Miller    25043.07     15

-How many customers bought products each year?

2018 is low because we only have data from the month of January

   year  Total number of Customers
0  2014                        589
1  2015                        578
2  2016                        633
3  2017                        691
4  2018                         20

![How many customers bought products each year](https://github.com/LorenzoBelenguer/Superstore-sales-enquiries/assets/82720058/e8d443a3-4175-4693-bfed-63fa663cdbe8)


-How many customer segments there are in the dataset?

3

