# Product Matching
Matching products from Flipkart on Amazon and print prices to compare them.

We have two datasets of products from Flikart and Amazon, each having 20001 rows of Product name, URL, Retail price, Discounted price, Image and Unique ID.

Here, our Unique ID is the product key.

## Data Cleaning

Checking for null values in the retail price was done. Then, their indices were extracted and the rows of those indices were dropped from both datasets.

## Product Matching

A left join of Flipkart and Amazon dataset is done using pd.merge(). The left join is done on the uniq_id column. Left join takes all uniq_id values from flipkart and then match the same with amazon. So, in the end, only the matched same rows of uniq_id are available.

Next, the unncessary columns were dropped using df.drop()

The column names were changed.

The output has to look like:

