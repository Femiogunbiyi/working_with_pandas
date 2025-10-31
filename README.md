
Working with Pandas DataFrames is fundamental for data manipulation and analysis in Python. Here's a summary of key aspects:
1. What is a DataFrame?
A Pandas DataFrame is a two-dimensional, tabular data structure with labeled rows (index) and labeled columns. It's similar to a spreadsheet or a SQL table, allowing for efficient storage and manipulation of heterogeneous data types within different columns. 
2. Creating DataFrames:

    From a dictionary: A common method is to create a dictionary where keys are column names and values are lists of data for each column. This dictionary is then passed to pd.DataFrame(). 

Python

    import pandas as pd
    data = {'Name': ['Alice', 'Bob'], 'Age': [25, 30]}
    df = pd.DataFrame(data)
    print(df)

    From external sources: DataFrames can be created by reading files like CSV, Excel, or SQL databases using functions like pd.read_csv(), pd.read_excel(), or pd.read_sql(). 

3. Accessing Data:

    Columns:
    Access a column using bracket notation with the column name (e.g., df['ColumnName']). This returns a Pandas Series.
    Rows:
        .loc (location by label): Select rows based on their index labels (e.g., df.loc['row_label']).
        .iloc (integer location): Select rows based on their integer position (e.g., df.iloc[0] for the first row). 

4. Modifying DataFrames:

    Adding/Updating Columns:
    Assign a new list or Series to a new column name using bracket notation (e.g., df['NewColumn'] = [value1, value2]). You can also update existing columns similarly.
    Adding Rows:
    Create a new DataFrame (even a single row) and use pd.concat() to append it to the original DataFrame.
    Handling Missing Data:
    Functions like isnull(), notnull(), dropna(), and fillna() are used to identify, remove, or fill missing values (NaN). 

5. Common Operations:

    Sorting: df.sort_values(by='ColumnName') sorts the DataFrame by a specified column.
    Filtering: Use boolean indexing to select rows that meet specific conditions (e.g., df[df['Age'] > 25]).
    Statistical Methods: Apply statistical functions like mean(), sum(), max(), min() to columns or the entire DataFrame.
    Applying Functions: Use .apply() to apply a custom function along rows or columns. 

6. DataFrame Properties:

    .shape: Returns a tuple representing the dimensions (rows, columns).
    .columns: Returns an Index object containing column labels.
    .index: Returns the row index.
    .dtypes: Returns the data types of each column.
