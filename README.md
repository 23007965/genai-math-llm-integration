## Integration of a Mathematical Calulations with a Chat Completion System using LLM Function-Calling

### AIM:
To design and implement a Python function for retrieving the exchange rate of a currency and integrate it with a Chat Completion System using the Function Calling feature of a Large Language Model (LLM).

### PROBLEM STATEMENT:
Develop a Python application that uses the Function Calling capability of an LLM to identify a user's request for a currency exchange rate. The LLM should automatically invoke a predefined Python function that returns the exchange rate of the requested currency in JSON format. This demonstrates how LLMs can interact with external functions to provide structured and reliable information.

### DESIGN STEPS:

#### STEP 1:
Import the required Python libraries (openai, json, os, and dotenv) and configure the OpenAI API key.

#### STEP 2:
Create a Python function get_exchange_rate(currency) that stores sample exchange rates in a dictionary and returns the corresponding exchange rate in JSON format.

#### STEP 3:
Define the function schema, send the user's query to the Chat Completion API, allow the LLM to invoke the appropriate function, parse the function arguments, execute the Python function, and display the JSON response.

### PROGRAM:

### OUTPUT:

### RESULT:
