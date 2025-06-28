
# Employee Data Validation with Pydantic

This project demonstrates how to validate employee data in Python using **Pydantic**, a powerful data validation and parsing library.

## What is Pydantic?

Pydantic helps you define data models using Python’s type hints and automatically validates data against those types. It uses the `BaseModel` class to create structured data models. You can also write custom validation logic using decorators like `@field_validator`.

## What This Project Does

* Defines an `Employee` model with fields like `name`, `age`, `email`, `department`, and `employee_id`.
* Uses Pydantic’s built-in `EmailStr` type to ensure emails are valid.
* Implements a custom validator to check that the `employee_id` is exactly 6 alphanumeric characters.
* Loads employee data from a JSON file and validates each record.
* Prints valid records and detailed errors for invalid records.

## How to Run

1. Install dependencies:

```bash
pip install pydantic[email]
```

2. Make sure your employee data file (e.g., `employees.json` or `employees.json.txt`) is in the correct directory.

3. Run the Python script:

```bash
python main.py
```

## Example Output

```
Valid employee record: John Doe
Valid employee record: Jane Smith
Invalid employee record: Alice Brown
Errors: [{'loc': ('email',), 'msg': 'value is not a valid email address', ...}]
Valid employee record: Dave West
```

