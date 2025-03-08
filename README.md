# Chatbot_using_NLP
Implementation of chatbot using NLP


```markdown
# Simple Chatbot with Streamlit

This project implements a basic chatbot using NLTK, scikit-learn, and Streamlit. The chatbot is designed to respond to a variety of user queries based on predefined intents.

## Prerequisites

Before running the code, ensure you have the following installed:

-   Python 3.6+
-   pip (Python package installer)

Install the required Python packages using pip:

```bash
pip install nltk scikit-learn streamlit
```

## Setup

1.  **Download NLTK Data:**
    * The code downloads the NLTK `punkt` resource during runtime. However, if you encounter issues, you can manually download it:
        ```python
        import nltk
        nltk.download('punkt')
        ```
    * If you encounter a `LookupError: Resource punkt_tab not found` error, you will also need to download that resource:
        ```python
        import nltk
        nltk.download('punkt_tab')
        ```
2.  **Run the Streamlit App:**
    * Save the provided code as a Python file (e.g., `chatbot.py`).
    * Open a terminal or command prompt and navigate to the directory where you saved the file.
    * Run the Streamlit app:
        ```bash
        streamlit run chatbot.py
        ```
    * Streamlit will open a web browser window displaying the chatbot interface.

## Functionality

The chatbot is trained on a set of predefined intents, which include:

-   Greetings
-   Goodbyes
-   Thanks
-   About
-   Help
-   Age
-   Weather
-   Budget
-   Credit score
-   Time
-   Jokes
-   Recommendations

When you enter a message, the chatbot uses a TF-IDF vectorizer and a Logistic Regression classifier to determine the intent of your message. It then selects a random response from the corresponding intent's responses.

## Code Explanation

1.  **Install Dependencies:**
    * The first cell installs the necessary Python packages.
2.  **Import Libraries:**
    * The code imports `nltk`, `random`, `os`, `ssl`, `streamlit`, `TfidfVectorizer`, and `LogisticRegression`.
3.  **NLTK Setup:**
    * The SSL context is modified to avoid potential SSL certificate issues.
    * The NLTK data path is appended to ensure that NLTK can find the downloaded resources.
    * The `punkt` tokenizer is downloaded.
4.  **Define Intents:**
    * The `intents` list contains dictionaries, each representing an intent with its `tag`, `patterns`, and `responses`.
5.  **Create Vectorizer and Classifier:**
    * A `TfidfVectorizer` is created to convert text patterns into numerical vectors.
    * A `LogisticRegression` classifier is created for intent classification.
6.  **Preprocess Data:**
    * The code extracts the `tags` and `patterns` from the `intents` data.
7.  **Train the Model:**
    * The `TfidfVectorizer` is used to transform the `patterns` into TF-IDF vectors.
    * The `LogisticRegression` classifier is trained on the TF-IDF vectors and corresponding tags.
8.  **Create Streamlit Interface:**
    * A Streamlit interface is created with a title and a text input field.
    * When the user enters a message, the code predicts the intent and selects a random response.
    * The user's message and the chatbot's response are displayed in the Streamlit app.

## Usage

1.  Open the Streamlit app in your web browser.
2.  Type a message in the text input field and press Enter.
3.  The chatbot will respond with a relevant message.

## Notes

-   The chatbot's responses are based on predefined intents. To improve the chatbot's accuracy and versatility, you can add more intents and patterns.
-   The model is simple and can be improved with more complex NLP techniques.
-   If you have issues with NLTK data downloading, manually downloading the required NLTK resources is recommended.
```
