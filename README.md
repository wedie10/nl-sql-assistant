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
**Question:** Average loan amount by tenure for active loans
**Result:** 
tenure_months	avg(loan_amount)
0	12	266366.390963
1	24	256755.500000
2	36	261705.804082
3	48	255488.691837
4	60	261639.869888

## Run it
1. `pip install duckdb pandas google-genai`
2. Open `nl_sql_assistant.ipynb`
3. Run all cells and paste your Gemini API key when prompted

## Notes
The dataset is synthetic, generated in the notebook for demonstration.