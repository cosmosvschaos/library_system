# Preparing for the Project

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

During the club session, go over the plans, formats of the tables(database) function signatures, and descriptions with your teammates. This ensures everyone is on the same page and understands their tasks. Encourage discussions and suggestions for improvements at this stage to prevent issues later in the project timeline.
