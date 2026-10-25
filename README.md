# Basic Data Validation – Employee Data Entry Template

**Task 25 – Basic Data Validation**
Veda Technology | Data Analytics Track | Level 1, Day 25

## About
I built a data-entry template for employee records in Excel. It uses dropdown lists and validation rules so that wrong values are rejected as they are typed, which keeps the data clean. The 15 sample entries are made-up (synthetic) employee data.

## Workbook structure
| Tab | What it does |
|-----|--------------|
| How to fill | Short instructions and the rule for each column |
| Employee Entry | The data-entry sheet with the validation rules and 15 sample entries (yellow cells are the input cells) |
| Lists | The options that feed the dropdowns (department, job level, status) |
| Test Log | The invalid values I tried and what happened |

## Validation rules
| Column | Rule | Type |
|--------|------|------|
| Employee ID | `EMP` + 3 digits (for example EMP016), and must be unique | Custom formula |
| Full Name | 2 to 50 characters | Text length |
| Department | Sales, Marketing, Finance, HR, IT, Operations | Dropdown list |
| Job Level | Junior, Mid, Senior, Manager | Dropdown list |
| Hire Date | A real date from 2015-01-01 up to today (no future dates) | Date |
| Monthly Salary | A number from 20,000 to 300,000 | Decimal |
| Email | Must contain `@` and a dot after it, with no spaces | Custom formula |
| Performance Rating | Whole number from 1 to 5 | Whole number |
| Status | Active, On Leave, Resigned | Dropdown list |

## Clear labels and messages
- Each column heading has a hover note that explains its rule
- Each input cell shows a short input message when it is selected
- Each rule has its own error message that says what went wrong and how to fix it
- A "How to fill" tab explains the whole template

## How I tested it
I typed an invalid value into each rule to check that Excel rejects it. The full list is in the `Test Log` tab.

| Column | Invalid value tried | Result |
|--------|--------------------|--------|
| Employee ID | `EMP1` | Rejected |
| Employee ID | `EMP001` (already exists) | Rejected |
| Full Name | `A` | Rejected |
| Department | `Cooking` | Rejected |
| Hire Date | A future date | Rejected |
| Monthly Salary | `5000` | Rejected |
| Email | `maya.example.com` (no @) | Rejected |
| Performance Rating | `6` | Rejected |
| Performance Rating | `3.5` | Rejected |
| Status | `Retired` | Rejected |

## What I learned
- Data validation stops mistakes at the moment of entry, which is much easier than cleaning data later
- Dropdowns remove spelling mistakes and different names for the same thing (like "HR" and "Human Resources")
- Custom formulas can check things that the built-in rules cannot, like a duplicate ID or an email format
- Clear error messages help the person fix the problem straight away

## Files
- `Employee_Entry_Template.xlsx` – the validated template with sample entries
- `validation_screenshot.png` – screenshot of a dropdown and an error message
- `README.md`

## Tools used
Microsoft Excel (Data Validation: list, date, decimal, whole number, text length and custom rules)

## Author
Rabia
