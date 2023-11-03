# Text Classification for Brand Detection

List any prerequisites that are required to run the project. For example:

- Python 3.7 or higher
- [List any other dependencies or packages]

## Usage

1. Train the model:

2. Start the server:


3. Make a POST request to the server:
- You can make a POST request to the server using tools like `curl`. For example:
  ```
  curl -d '{"text": "Sample text to classify"}' -H "Content-Type: application/json" -X POST http://0.0.0.0:55555/brand
  ```

4. Receive the predicted brand label and probability in the response.

## Server

Listening for Requests: The server continuously listens for incoming HTTP requests, specifically POST requests. These requests should contain a JSON payload with a 'text' field, which represents the input text that needs to be classified.

Text Classification: When a POST request is received, the server processes the 'text' from the request and sends it to the trained text classification model for prediction. The model predicts the brand associated with the input text.

Response: The server then constructs a JSON response containing the predicted brand label and the associated probability. This response is sent back to the client that made the request.

## Model Performance

After training and evaluating the text classification model, it's essential to assess its performance on a validation dataset.


Accuracy: 0.9427012278308322
Classification Report:
              precision    recall  f1-score   support

       chase       1.00      0.97      0.98        87
      costco       0.98      0.98      0.98       266
   microsoft       0.88      0.99      0.93       158
     netflix       0.90      0.85      0.88        75
     opensea       0.94      0.94      0.94        99
       steam       1.00      0.77      0.87        31
       tesco       0.00      0.00      0.00         2
     walmart       0.82      0.60      0.69        15

    accuracy                           0.94       733
   macro avg       0.81      0.76      0.78       733
weighted avg       0.94      0.94      0.94       733


