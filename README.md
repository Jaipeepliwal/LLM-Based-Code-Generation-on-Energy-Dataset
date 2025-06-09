Name - JAI PEEPLIWAL

Groq - llama-3 was used

Summary:
This jupyter notebook uses a Large Language Model (LLM), particularly Groq API and LLaMa 3 to convert natural language 
queries into executable Python code using UCI Household Power Consumption Dataset.
The core steps/code used in this notebook are as follows:
1. Loading Dataset and Preprocessing:
    a. The dataset is loaded using pandas.
    b. Missing values were removed
    c. The datetime column was created from Date and Time, and set as the index.
    d. Column - Global_active_power was converted to float.

2. Groq API and LLM integration:
    a. The environment variable "GROQ_API_KEY" set with API key in .env file.
    b. It uses ChatGroq class from langchain_groq package to access "LLaMa 3.1-8B-Instant" model.
    c. This model have 8 Billions parameters and optimized for speed.
    d. The parameters used are "temperature=1.0" which is used to control randomness in output and "max_retries=2" which is used if a request fails the system retries up to 2 times.

3. The Natural Language Queries and their Code Execution:
    a. Average active power in March 2007
    b. Hour with highest usage on Christmas 2006
    c. Compare weekday vs weekend usage
    d. Find days where consumption > 5KWh
    e. Plot energy trend from Jan 1 2007 to Jan 7 2007
    f. Average voltage in first week of February 2007
    g. Correlation between Global_active_power and sub_metering
    h. Each response was validated, corrected, and executed.
