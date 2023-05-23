# Clothing Similarity Search Project
This project aims to create a machine-learning model capable of receiving text describing a clothing item and returning a ranked list of links to similar items from different websites. The solution is implemented as a function deployed on Google Cloud that accepts a text string and returns JSON responses with ranked suggestions.

## Project Overview

The project involves the following steps:
### Data Collection and Preprocessing:

1. The Myntra Fashion Product Dataset is used, which can be obtained from this Kaggle link.
2. The dataset is preprocessed to clean the text data by converting it to lowercase, removing special characters, and punctuation, and handling missing values.
### Feature Extraction and Similarity Measurement:

1. Text descriptions are converted into numerical representations using the TF-IDF (Term Frequency-Inverse Document Frequency) technique.
4. The similarity between the input text and the texts in the dataset is computed using cosine similarity.
### Ranking and Result Generation:

A function is designed to accept a text string, extract its features, compute similarities with the items in the dataset, rank them based on similarity, and return the URLs of the top-N most similar items in JSON format.
### Deployment:

The function is deployed on Google Cloud Functions or Google Cloud Run to provide an HTTP endpoint that accepts POST requests and returns JSON responses.

## Instructions for Deployment
To deploy the Clothing Similarity Search function on Google Cloud, follow these steps:
### Set up a Google Cloud project:

1. Create a new project or use an existing one.
2. Enable the necessary APIs: Cloud Functions or Cloud Run, depending on your preferred deployment method.
### Prepare the function code:

1. Copy the relevant code for data preprocessing, feature extraction, similarity measurement, and result generation into your project directory.
2. Install the required dependencies, including scikit-learn and other necessary libraries.
3. Create a requirements.txt file listing the required dependencies.
### Deploy the function:
1. Define an HTTP trigger for the function.
2. Use the gcloud command-line tool or the Google Cloud Console UI to deploy the function from your project directory, specifying the necessary parameters.
3. Note the endpoint URL provided upon successful deployment.
### Test the deployed function:

1. Use an HTTP client (e.g., cURL, Postman) to send a POST request to the function's endpoint URL.
2. The request body should contain a JSON object with a text field representing the clothing item description.
3. The response will contain a JSON array with the top-N most similar items, including their name, URL, and similarity score.
### Iterate and refine:

Test the function with various input texts to evaluate the results and make adjustments as necessary.
