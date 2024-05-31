
# jmock: Generate Synthetic Data with the Power of AI
jmock is a Python package that leverages the power of AI to generate realistic and diverse synthetic data for testing purposes. It simplifies the process of creating mock data for your applications, especially when dealing with large datasets or third-party integrations.


## Authors

- [@joepeter-francis](https://github.com/joepeter-francis)


## Features

- AI-Driven Data Generation: Utilize the capabilities of Google's Generative AI to create unique and varied data that closely resembles real-world scenarios.
- Flexibility: Generate data in various formats, including as an array of objects or JSON strings, to suit your testing needs.
- Customization: Control the amount of data generated and the level of variation through the count and VARIATION parameters.
- History Tracking: Prevent duplicate data by keeping track of previously generated values and ensuring uniqueness.


## Installation

Install jmock using pip

```bash
  pip install jmock
```
    
## Usage/Examples
- Import the necessary modules:
```python
import jmock as jm
```
- Load your environment variables:
```python
from dotenv import load_dotenv
load_dotenv()
```
- Set your Google API key and Variation value (between 0-1):
```python
GOOGLE_API_KEY = os.environ.get('GOOGLE_API_KEY')
VARIATION = os.environ.get('VARIATION')
```
- Generate synthetic data:
```python
sample = {
    'name': 'Joe', 
    'Id': '6FGU890128', 
    'email': 'joe@microsoft.com', 
    'company': 'microsoft', 
    'website': 'microsoft.com', 
    'Status': True, 
    'address': {
        'city': 'bangalore', 
        'pincode/zipcode': 560010
        }}
count = 5
result = jm.dataAsString(sample,count,GOOGLE_API_KEY,VARIATION)
print(result)
```
- Example Output:
```json
[{
    "name": "Liam",
    "Id": "7HJG678291",
    "email": "liam@apple.com",
    "company": "apple",
    "website": "apple.com",
    "Status": False,
    "address": {
      "city": "pune",
      "pincode/zipcode": 411027
    }
  }
  # ... 4 more unique objects]
  ```
## Related
[How to generate gemini API key](https://www.geminiforwork.com/setup-api-keys/create-geminiai-api-key/)

