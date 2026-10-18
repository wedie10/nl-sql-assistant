# Natural-Language Analytics Assistant

Ask questions about a loan dataset in plain English and get back the SQL, the result table, and a short written summary.

## How it works
1. A question is sent to an LLM (Gemini API) together with the table schema.
2. The model returns a DuckDB SQL query.
3. A safety check allows read-only SELECT queries only.
4. The query runs on the data and the result is summarised in plain English.

## Tech
Python, Pandas, DuckDB, Gemini API, Jupyter

## Example
**Question:** What is the default rate by loan grade?
**Result:** Default rate rises from about 10% (grade A) to over 98% (grade G).

## Run it
1. `pip install duckdb pandas google-genai`
2. Open `nl_sql_assistant.ipynb`
3. Run all cells and paste your Gemini API key when prompted

## Data
Credit risk dataset from Kaggle (32,581 loan applicants; 12 columns including income, loan grade, loan amount and default status). Source: Kaggle "Credit Risk Dataset".