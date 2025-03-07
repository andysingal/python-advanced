```py
import logging
import requests

# Configure logging
logging.basicConfig(level=logging.DEBUG)
logger = logging.getLogger(__name__)

# Function to log request details
def log_request_body(response, *args, **kwargs):
    logger.debug(f"Request URL: {response.request.url}")
    logger.debug(f"Request Headers: {response.request.headers}")
    logger.debug(f"Request Body: {response.request.body}")

# Example request
url = "https://your-azure-search-endpoint"
headers = {
    'Content-Type': 'application/json',
    'api-key': 'REDACTED',
    'Accept': 'application/json;odata.metadata=none'
}
data = '{"your": "request body"}'

# Send request with hooks to log the request body
response = requests.post(url, headers=headers, data=data, hooks={'response': log_request_body})
```
