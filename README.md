# Address Formatter MX

Address Formatter MX is a project that focuses on reformatting Mexican property addresses to follow a standardized structure commonly used by lawyers and notaries. The goal is to develop a fine-tuned Large Language Model (LLM) that can take inconsistently formatted addresses as input and generate properly formatted addresses as output.

## Key Features

- Fine-tuning of a pre-trained LLM (StableLM 2 1.6B) on a dataset of Mexican property addresses.
- Preprocessing of raw address data to create a supervised training dataset.
- Training and evaluation of the fine-tuned model using Google Colab for GPU/TPU acceleration.
- Development of a FastAPI application to serve the model as an API endpoint.
- Integration with ngrok for exposing the API running on Google Colab.

## Dataset

The project utilizes a dataset of 1,336 Mexican property addresses in a CSV format. The dataset undergoes preprocessing to create a supervised training dataset, where each raw address is mapped to its correctly formatted counterpart. This dataset is then used to fine-tune the StableLM model.

# Model

The chosen model for this project is StableLM 2 1.6B, a multilingual model that includes Spanish. By fine-tuning this model on the preprocessed address dataset, the model learns to reformat Mexican property addresses into the desired standardized format.

# API

The fine-tuned model is served as an API using FastAPI. The API provides an endpoint that accepts a raw Mexican property address as input and returns the formatted address as output. The API is designed to be easily integrated into other applications or systems that require consistent and standardized address formatting.

# Usage

To use the Address Formatter MX project, follow these steps:

1. Clone the repository: ```git clone https://github.com/your-username/address-formatter-mx.git```
2. Install the required dependencies: ```pip install -r requirements.txt```
3. Preprocess the raw address dataset using the provided scripts in the ```src/data``` directory.
4. Fine-tune the StableLM model using the Jupyter notebook in the ```notebooks``` directory.
5. Run the FastAPI application using the script in the ```src/api``` directory.
6. Expose the API using ngrok for external access.
7. Make POST requests to the API endpoint with the raw address as input to receive the formatted address as output.

# Contributions

Contributions to the Address Formatter MX project are welcome! If you encounter any issues, have suggestions for improvements, or would like to add new features, please submit a pull request or open an issue on the GitHub repository.

# License

This project is licensed under the MIT License.

---

# Project Structure

address-formatter-mx/
│
├── data/
│   ├── raw/
│   │   └── original_addresses.csv
│   └── processed/
│       └── formatted_addresses.csv
│
├── models/
│   └── stablelm_finetuned/
│
├── notebooks/
│   └── address_formatting.ipynb
│
├── src/
│   ├── data/
│   │   ├── __init__.py
│   │   └── preprocess.py
│   ├── models/
│   │   ├── __init__.py
│   │   └── train.py
│   └── api/
│       ├── __init__.py
│       └── app.py
│
├── tests/
│   └── test_address_formatting.py
│
├── requirements.txt
├── README.md
└── .gitignore