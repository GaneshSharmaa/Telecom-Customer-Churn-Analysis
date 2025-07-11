# Telecom Customer Churn Analysis
Hey guys, this is an EDA project where I explored telecom customers' churn data, which was available in the form of a CSV file.<br>

The dataset consisted of customer details such as:
- CustomerID
- Gender
- Senior citizen or not
- Partner or not
- Service tenure (in months)
- Services (such as phone services, multiple lines services, internet services, online security, device protection, tech support, streaming TV, and movies)
- Contract type (monthly, yearly, etc.)
- Paperless billing or not
- Payment method
- Monthly charges
- Total charges
- Churned or not

First, I loaded the dataset into a DataFrame, then I checked the summary of each column (number of rows, number of non-null values, data types, etc.).<br>

Then, I looked for empty values and found that there were no null values, which saved me from taking care of missing values.<br>

I noticed then the `TotalCharges` column had 'object' data-type values, I looked for starting rows of `TotalCharges` column and found entire column has filled with a blank value ` `, then I replaced the ` ` value with a string `"0"` value, and then changed it's data type to float by using `astype()` method.<br>

Then, I looked for the number of null values over the entire DataFrame and found that there were no missing values, so I was good to proceed further.<br>

Then, I tried to have a descriptive look at the DataFrame by using the `describe()` method on the DataFrame.<br>

Had a look at duplicate values over an entire DataFrame, and there were no duplicate values. I specifically checked for duplicate values in the `customerID` column, since every customer will have a unique customer ID. If there have been any duplicacies in the `customerID`, then that entire row would have been a duplicate.<br>

Column `SeniorCitizen` had values in integer, in the dataset if they wanted to represent a customer with them being a senior citizen they used `0` and `1` binary values for representing that, with `0` meaning they're not a senior citizen and `1` meaning customer is a senior citizen. This was resulting in confusion, and this would also create a problem while plotting the data, so I decided to change these binary `0` and `1` values to `No` and `Yes`, respectively. This change was done with the help of a function I made, `convert(value)`, which took each value in the column as a function parameter and then, by using the conditional change, converted the values to `Yes` and `No`.<br>

Then, I started using Matplotlib and the Seaborn library for visualization purposes.
