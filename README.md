# STUDENT DETAILS 
## ***SAJID RAZAQ*** 
## ***BASAI-F24-049***
# ***PF PROJECT PRESENTATION***

## PANDAS LIBRARAY

* The pandas library is one of the most popular Python libraries for working with structured data. It is widely used for data analysis, manipulation, and cleaning, offering intuitive tools to handle everything from small datasets to large-scale, complex data
  
# BASIC OPERATION

#  LOADING DATA
* Loading data in the pandas library means importing external data files (like CSV, Excel, JSON, SQL, etc.) into a DataFrame (a table-like structure in pandas) for processing and analysis. This is the first step in working with data using pandas
  
# STEP FOR DATA LOAD IN PANDAS
* Steps to Load Data in pandas:
* Import the pandas Library
* Start by importing pandas:

* python
* Copy
* Edit
* import pandas as pd
* Choose the File Type
* Depending on the type of file you’re working with (e.g., CSV, Excel, JSON), use the appropriate pandas function to load the data into a DataFrame.
  
# IMPORET PANDAS AS PD
* The line import pandas as pd is a Python command used to import the pandas library and give it the short alias pd. This alias makes it easier and faster to use the library's functions in your code

# IMPORT MATPLOTLIB AS PLT
* The line import matplotlib as plt is a Python command used to import the matplotlib library, which is widely used for creating visualizations and plots in Python.


# df=pd.read_csv("country_wise_latest.csv",encoding= 'latin')
# print(df)

* The code loads the CSV file "country_wise_latest.csv" into a pandas DataFrame.
* It specifies the encoding as 'latin' to handle special characters correctly.
* Then it prints the DataFrame to display the data.

# df=pd.read_csv("country_wise_latest.csv",encoding= 'latin')
# print(df.to_string())

* pd.read_csv() reads the CSV file into a DataFrame.
* to_string() ensures the full DataFrame is displayed as a string.
* print() prints that full string representation of the DataFrame.


# df=pd.read_csv("country_wise_latest.csv",nrows=1)

* pd.read_csv("country_wise_latest.csv", nrows=1): Reads the first row of the CSV file. The nrows=1  parameter ensures only the first row of the file is read.

# df=pd.read_csv("country_wise_latest.csv",skiprows=1)


* pd.read_csv("country_wise_latest.csv", skiprows=1):

* Reads the CSV file but skips the first row of the file.
* The skiprows=1 argument tells pandas to exclude the first row when reading the data.
* print(df.to_string()):
# df=pd.read_csv("country_wise_latest.csv",index_col="Country/Region")

* This code reads the CSV file country_wise_latest.csv and sets the "Country/Region" column as the DataFrame index. This makes it easier to access rows using country names as keys


# df[100:111]

* Slicing behavior: In pandas, the slicing syntax [start:end] includes the start index (100) but excludes the end index (111), so it retrieves rows 100 to 110.
Output: It will return the data for these 11 rows, including all columns.

* print(df.to_string()): Converts the DataFrame df into a string and prints it in a readable format
# df.head()
* df: This is your DataFrame, which contains your data.
* .head(): This is a method in pandas that shows the first 5 rows of the DataFrame by default

# df.tail()
* df: This is your DataFrame, which holds your data.
* .tail(): This is a pandas method that shows the last 5 rows of the DataFrame by default

# df.info()
* df: This is your DataFrame, the table-like structure containing your data.
* .info(): This method provides a quick overview of the DataFrame, including details about the columns, non-null values, and data types

# df.describe()
* df: This is your DataFrame, which contains your data.
* .describe(): This method calculates and shows summary statistics for the numeric columns in the /8  DataFrame, including measures like mean, standard deviation, and more

# df.columns
* It returns an Index object containing the labels of all the columns in the DataFrame.
* The column names are the headers or labels that define the fields in your DataFrame.


# df["Country/Region"]
* The phrase "Country/Region" in English refers to a location-based category, commonly used in databases, forms, or surveys to denote the country or region in which something or someone is located. In a dataframe context, it would represent the column where the geographical information (country or region) of the entities in the data is stored

# df.shape
* In the context of a DataFrame (commonly used in Python with libraries like pandas), df.shape is an attribute that returns the dimensions of the DataFrame. It gives the number of rows and columns in the format
  
# df.rename(columns={"Country/Region":"COUNTRY"})

* df: The DataFrame containing the data.
* rename(): A method used to modify the names of columns (or rows).
* columns: A parameter specifying that the renaming applies to the columns.
* {"Country/Region": "COUNTRY"}: A dictionary where the key is the current column name ("Country/Region") and the value is the new name ("COUNTRY").

# df["Deaths"]>30
* df["Deaths"]: Refers to the "Deaths" column in the DataFrame.
* > 30: This is a comparison operator checking whether the values in the "Deaths" column are greater than 30
   
# df[df["New recovered"]>1000]
* df: The DataFrame containing your data.
* df["New recovered"]: Refers to the "New recovered" column in the DataFrame.
* > 1000: A condition checking if the values in the "New recovered" column are greater than 1000

# df[df["Country/Region"]=="Bangladesh"]
* df: The DataFrame containing the data.
* df["Country/Region"]: Refers to the "Country/Region" column in the DataFrame.
* == "Bangladesh": A condition that checks whether the value in the "Country/Region" column is equal to "Bangladesh"

# df.sort_values(by="Deaths",ascending=True)
* df: The DataFrame containing your data.
* sort_values(): A method used to sort the DataFrame by one or more columns.
* by="Deaths": Specifies that the sorting should be done based on the "Deaths" column.
* ascending=True: This indicates that the sorting should be in ascending order (from lowest to highest)

# df.loc[9,"Deaths"]
* df: The DataFrame containing the data.
* .loc[]: A method used to access a group of rows and columns by labels or a specific value based on labels.
* 9: Refers to the row label (in this case, row index 9). This can be a numeric index or a label, depending on how your DataFrame is indexed.
* "Deaths": Refers to the column named "Deaths".
* So, df.loc[9, "Deaths"] will return the value in the "Deaths" column for the row at index 

# df.iloc[100]

* df: The DataFrame containing your data.
* .iloc[]: A method used to access rows or columns by their integer index position (starting from 0).
* 100: Refers to the 100th row in the DataFrame, based on its integer index position. (Remember, Python indexing starts from 0, so this is actually the 101st row in human terms.)

# df.dtypes
* df: The DataFrame containing your data.
* .dtypes: An attribute that returns the data types of each column in the DataFrame

# df["Confirmed"].mean()

*  df: The DataFrame containing your data.
* df["Confirmed"]: Refers to the "Confirmed" column in the DataFrame.
* .mean(): A method that calculates the mean (average) of the numerical values in the column

# df["Confirmed"].mode()

* df: The DataFrame containing your data.
* df["Confirmed"]: Refers to the "Confirmed" column in the DataFrame.
* .mode(): A method that returns the mode, which is the most frequent value(s) in the "Confirmed" column

# df.isnull()
* df: The DataFrame containing your data.
*.isnull(): A method that checks for null (missing) values in the DataFrame. It returns a DataFrame of the same shape, where each cell contains a boolean value:
* True if the value is missing (null).
* False if the value is not missing (i.e., it has a valid value)

# df.isnull().sum()

* df: The DataFrame containing your data.
* .isnull(): Checks for missing (null) values in the DataFrame, returning a DataFrame of the same size * nwith True for missing values and False for non-missing values.
* .sum(): Sums the boolean values (where True is treated as 1 and False as 0), which gives the total count of missing values for each column

# df.dropna()

* df: The DataFrame containing your data.
* .dropna(): A method that removes any rows (by default) with missing (null) values in any column.

# df.dropna(inplace=True)
* df: The DataFrame containing your data.
* .dropna(): The method used to remove rows or columns with missing (null) values.
* inplace=True: This option modifies the original DataFrame directly, rather than returning a new DataFrame. The operation is performed in place

# df.fillna(50000)
* df: The DataFrame containing your data.
* .fillna(): A method that replaces missing (null) values with a specified value or method.
* 50000: The value that will replace all NaN (Not a Number) or missing values in the DataFrame

# df["Deaths"].fillna(50)
* df: The DataFrame containing your data.
* df["Deaths"]: Refers to the "Deaths" column in the DataFrame.
* .fillna(50): Replaces all NaN (Not a Number) or missing values in the "Deaths" column with the value 50.

# print(df.duplicated())
* df: The DataFrame containing your data.
* .duplicated(): A method that identifies duplicate rows in the DataFrame. It returns a boolean

# df['col']=188
# df
* df: The DataFrame containing your data.
* df['col']: Creates a new column named "col". If this column already exists, it will update the existing values.
* 188: This value is assigned to every row in the new column "col"


# ***MAKING GRAPH TO HANDEL DATA***

#  01 df["Deaths"].plot(kind="bar")
* When you run this, it will create a bar chart where the x-axis corresponds to the index of the DataFrame (typically row numbers), and the y-axis represents the values from the "Deaths" column.

#  02 df["New cases"].plot(kind="pie")
* df: The DataFrame containing your data.
* df["New cases"]: Refers to the "New cases" column in the DataFrame.
* .plot(): A method that generates various types of plots.
* kind="pie": Specifies that the plot should be a pie chart

# 03 df["Deaths"].plot(kind='area')
* An area plot is similar to a line plot, but the area below the line is filled with color, making it useful for visualizing the cumulative value or overall trends in the data.

#  04 df["Deaths"].plot(kind="barh")
* df["Deaths"]: Refers to the "Deaths" column in the DataFrame.
* .plot(): A method that generates various types of plots.
* kind="barh": Specifies that the plot should be a horizontal bar plot


# 05 df["Deaths / 100 Cases"].plot(kind="kde")
* df: The DataFrame containing your data.
* df["Deaths / 100 Cases"]: Refers to the "Deaths / 100 Cases" column in the DataFrame.
*.plot(): A method that generates various types of plots.
* kind="kde": Specifies that the plot should be a Kernel Density Estimate (KDE) plot.

# 06 df["Deaths"].plot(kind="hist")
* df: The DataFrame containing your data.
* df["Deaths"]: Refers to the "Deaths" column in the DataFrame.
* .plot(): A method that generates various types of plots.
* kind="hist": Specifies that the plot should be a histogram

# 07 df["New deaths"].plot(kind="density")
* df: The DataFrame containing your data.
* df["New deaths"]: Refers to the "New deaths" column in the DataFrame.
* .plot(): A method that generates various types of plots.
* kind="density": Specifies that the plot should be a density plot or Kernel Density Estimate (KDE)

# 08 df["Deaths"].plot(kind="line")
* df: The DataFrame containing your data.
* df["Deaths"]: Refers to the "Deaths" column in the DataFrame.
* .plot(): A method that generates various types of plots.
* kind="line": Specifies that the plot should be a line plot

# 09 df["Confirmed last week"].plot(kind="box")
* df: The DataFrame containing your data.
* df["Confirmed last week"]: Refers to the "Confirmed last week" column in the DataFrame.
* .plot(): A method that generates various types of plots.
* kind="box": Specifies that the plot should be a box plot
