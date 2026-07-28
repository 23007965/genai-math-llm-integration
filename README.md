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
```python
import os
import openai

from dotenv import load_dotenv, find_dotenv
_ = load_dotenv(find_dotenv()) 
openai.api_key = os.environ['OPENAI_API_KEY']
```
```python
import json

def get_exchange_rate(currency):
    """Get the exchange rate of a currency to INR"""

    exchange_rates = {
        "USD": 87.50,
        "EUR": 102.30,
        "GBP": 118.40,
        "JPY": 0.59
    }

    result = {
        "currency": currency,
        "exchange_rate": exchange_rates.get(currency, "Not Available"),
        "base_currency": "INR"
    }

    return json.dumps(result)
```
```python
functions = [
    {
        "name": "get_exchange_rate",
        "description": "Get the current exchange rate of a currency to INR.",
        "parameters": {
            "type": "object",
            "properties": {
                "currency": {
                    "type": "string",
                    "description": "Currency code (e.g., USD, EUR, GBP, JPY)"
                }
            },
            "required": ["currency"]
        }
    }
]
```


### OUTPUT:

### RESULT:
