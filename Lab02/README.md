# Lab Session 2: Working with Dictionary and DataFrame

## Part I: Working with Dictionary

A dictionary is a data structure used to store data in **key-value pairs**.

### Example

```python
student = {
    "name": "Ram",
    "age": 20,
    "faculty": "BCE"
}
```

## Tasks: Dictionary Operations

| Operation               | Syntax                   | Example                  |
| ----------------------- | ------------------------ | ------------------------ |
| Create Dictionary       | `d = {}`                 | `d = {"a": 1, "b": 2}`   |
| Access Value            | `d[key]`                 | `d["a"]`                 |
| Use `get()`             | `d.get(key)`             | `d.get("a")`             |
| Add Item                | `d[key] = value`         | `d["c"] = 3`             |
| Update Value            | `d[key] = new_value`     | `d["a"] = 10`            |
| Remove Item using `del` | `del d[key]`             | `del d["b"]`             |
| Remove using `pop()`    | `d.pop(key)`             | `d.pop("a")`             |
| Remove Last Item        | `d.popitem()`            | `d.popitem()`            |
| Clear Dictionary        | `d.clear()`              | `d.clear()`              |
| Copy Dictionary         | `d.copy()`               | `new_d = d.copy()`       |
| Get All Keys            | `d.keys()`               | `d.keys()`               |
| Get All Values          | `d.values()`             | `d.values()`             |
| Get All Items           | `d.items()`              | `d.items()`              |
| Check Key Exists        | `key in d`               | `"a" in d`               |
| Get Length              | `len(d)`                 | `len(d)`                 |
| Loop Through Keys       | `for k in d:`            | `for k in d:`            |
| Loop Through Values     | `for v in d.values():`   | `for v in d.values():`   |
| Loop Through Items      | `for k, v in d.items():` | `for k, v in d.items():` |

---

# Part II: Working with Pandas DataFrame

A **DataFrame** in Python is a two-dimensional, tabular data structure that organizes data into labeled rows and columns.

It is conceptually similar to an **Excel spreadsheet** or an **SQL table**, making it the primary tool for data manipulation and analysis in the Pandas library.

## Tasks: DataFrame Operations

| Task                                                                                    | Syntax                                      |
| --------------------------------------------------------------------------------------- | ------------------------------------------- |
| Create a DataFrame containing student details such as Name, Age, and Marks.             | `df = pd.DataFrame()`                       |
| Display the first 5 rows of the DataFrame.                                              | `df.head()`                                 |
| Display the last 5 rows of the DataFrame.                                               | `df.tail()`                                 |
| Find the total number of rows and columns in the DataFrame.                             | `df.shape`                                  |
| Display all column names in the DataFrame.                                              | `df.columns`                                |
| Display complete information about the DataFrame including data types and memory usage. | `df.info()`                                 |
| Generate a statistical summary of numerical columns in the DataFrame.                   | `df.describe()`                             |
| Select and display the Name column from the DataFrame.                                  | `df['Name']`                                |
| Select and display multiple columns such as Name and Marks.                             | `df[['Name', 'Marks']]`                     |
| Display the first row of the DataFrame using positional indexing.                       | `df.iloc[0]`                                |
| Display the first row of the DataFrame using label-based indexing.                      | `df.loc[0]`                                 |
| Access a specific cell value such as Marks of the first student.                        | `df.loc[0, 'Marks']`                        |
| Filter and display students whose Marks are greater than 80.                            | `df[df['Marks'] > 80]`                      |
| Filter and display students whose Age is greater than 20 and Marks are greater than 75. | `df[(df['Age'] > 20) & (df['Marks'] > 75)]` |
| Add a new column called Grade to the DataFrame.                                         | `df['Grade'] = ['A', 'B']`                  |
| Increase all students’ Marks by 5.                                                      | `df['Marks'] = df['Marks'] + 5`             |
| Update the Marks of Ram to 95 using a condition.                                        | `df.loc[df['Name'] == 'Ram', 'Marks'] = 95` |
| Remove the Age column from the DataFrame.                                               | `df.drop('Age', axis=1)`                    |
| Remove the first row from the DataFrame.                                                | `df.drop(0, axis=0)`                        |
| Sort the DataFrame by Marks in ascending order.                                         | `df.sort_values('Marks')`                   |
| Sort the DataFrame by Marks in descending order.                                        | `df.sort_values('Marks', ascending=False)`  |
| Concatenate two DataFrames vertically.                                                  | `pd.concat([df1, df2])`                     |
| Read data from a CSV file into a DataFrame.                                             | `pd.read_csv('file.csv')`                   |
| Write the DataFrame into a CSV file.                                                    | `df.to_csv('file.csv')`                     |
| Read data from an Excel file into a DataFrame.                                          | `pd.read_excel('file.xlsx')`                |
| Write the DataFrame into an Excel file.                                                 | `df.to_excel('file.xlsx')`                  |
