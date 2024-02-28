# How to preapre for collaborative programming project

### Step 1: Draw a flow chart of the whole program

You can create the flow chart using <https://app.diagrams.net/>

### Step 2: Create Empty Functions with Signatures in Comments in Different Files

In each function's comments, include the following information:

1. **Parameter Names and Types:** Describe the input values that the function expects.
2. **Return Value and Type:** Specify the output value and type that the function produces.
3. **Description/Functionality:** Provide a brief description of what the function is supposed to do.
4. **Preconditions:** List any requirements that must be met before calling the function.
5. **Postconditions:** Define guarantees about the state of the program after the function has executed.

For example:

```python
def update_log(s_id: str, isbn: str, date: str, is_returning: bool):
    """
    @Parameters: s_id (str), isbn (str), date (str), is_returning (bool)
    @Return Value: None
    @Description/Functionality:
    Updates the log file with the information of the book that is being borrowed or returned.
    Appends a line in the format of "s_id, isbn, date, is_returning" to the log file.
    @Preconditions: The log file must exist and be in the same directory as the program.
    @Postconditions: The log file will have a new line appended to it.
    """
    return
```

> This file is in update.py, and the function is `update_log`. The team member responsible for this function will develop the logic to update the log file with the information of the book that is being borrowed or returned.

The main function (`main.py`) will be developed by the project leader, and each file will be assigned to a team member, containing empty functions to be developed by the person.

### Step 3: Review Plans, Signatures, and Descriptions with Teammates in Club Session

During the club session, go over the flowchart, formats of the tables(database), function signatures, and descriptions with your teammates. This ensures everyone is on the same page and understands their tasks. Encourage discussions and suggestions for improvements at this stage to prevent issues later in the project timeline.

### TIPS:

1. Start with a *Simple* Prototype: Beginning with a smaller and simpler plan allows you to iterate quickly and get feedback early in the development process. This agile approach enables you to identify and address issues sooner, and everyone understands the project better

2. Limit Global Variables: Minimizing the use of global variables helps avoid unintended side effects and makes your code easier to debug. Instead, passing variables as parameters to functions and use return values can lead to more safe and maintainable code.

3. Use Constants: Using constants instead of hardcoding numbers directly into your code makes it more readable and maintainable. By giving them descriptive names and storing them as constants, you make it easier to understand the purpose of those values and modify them later if needed. For example: 
> `PERIOD = 3`

4. Consider using Visual Studio Code. It's so much powerful and efficient

5. Consider using Pandas for database
You can store the DataFrame to a file using the `to_csv()` method in pandas. Here's how you can modify the previous code to save the DataFrame to a CSV file:

```python
import pandas as pd

# Create an empty DataFrame with columns
df = pd.DataFrame(columns=['s_id', 'isbn', 'date', 'is_returning'])

# Display empty DataFrame
print("Empty DataFrame:")
print(df)
print()

# Add entries to the DataFrame
new_entries = [
    {'s_id': '1', 'isbn': '978-0143129321', 'date': '2024-02-28', 'is_returning': True},
    {'s_id': '2', 'isbn': '978-0553380163', 'date': '2024-02-27', 'is_returning': False},
    {'s_id': '3', 'isbn': '978-1400031366', 'date': '2024-02-26', 'is_returning': True},
    {'s_id': '4', 'isbn': '978-0743273565', 'date': '2024-02-25', 'is_returning': False},
    {'s_id': '5', 'isbn': '978-0553380156', 'date': '2024-02-24', 'is_returning': True}
]

for entry in new_entries:
    df = df.append(entry, ignore_index=True)

# Display DataFrame with new entries
print("DataFrame with new entries:")
print(df)
print()

# Save DataFrame to a CSV file
df.to_csv('data.csv', index=False)

print("Data saved to 'data.csv' file.")
```

This code will save the DataFrame to a file named 'data.csv' in the current directory without including the index column. You can change the filename or path as needed.
