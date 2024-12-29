# API Usage Documentation

Welcome to the API usage documentation. This API allows users to query and retrieve information related to test data. Below is a detailed guide on the types of questions you can ask and how to interact with the API.

## Query Types

### 1. User Personal Information
You can inquire about personal health-related questions, which include:
- Overall health status
- Allergies
- Health goals
- Vaccination information
- Health conditions
- Medical equipment usage
- Medication schedule
- Medical procedures

**Important Note:** When asking personal questions, it's essential to provide the exact name along with the question. Currently, privacy concerns are not considered, but in the future, user information will be segregated in the knowledge base to protect privacy.

### 2. Specific ID Information
You can request information related to specific IDs, such as:
- Details of a consultation with a given `encounter_id`
- Observation details for a specific ID like `a-80000.vitalamb-159871`

### 3. Medical Resource Query
You can also query about available medical resources, such as:
- Finding obstetrics and gynecology clinics near Los Angeles

## API Endpoint

The service is hosted at: `http://18.219.230.164/api/question`

### Example Request

Below is an example of how to make a request to the API:

```python
import requests

url = "http://18.219.230.164/api/question"
payload = {
    "user_question": "I'm Medlock John, can you give me my patient summaries and insights?"
}

print("User Question:", payload["user_question"])
print("-" * 50)

# Send POST request
response = requests.post(url, json=payload, headers={"Content-Type": "application/json"})

print("Response Text:", response.text)
print("Response JSON:", response.json())
```

## Testing

For testing purposes, refer to the `test.ipynb` file. It contains a variety of sample questions and quick test code snippets to help you get started with the API.

We hope this documentation provides a clear understanding of how to use the API. If you have any questions or require further assistance, please feel free to reach out.