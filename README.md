# Chatbot for Immigration Document Processing

This Flask-based application processes images sent via Twilio WhatsApp, extracts text using OCR, anonymizes sensitive information, and summarizes the content using a local Llama 3 model. It also allows users to ask questions about the extracted content.

## Prerequisites

Before running this application, ensure you have the following:

-   Python 3.6+
-   [Ollama](https://ollama.com/) installed and running with the Llama 3 model available.
-   A Twilio account with a WhatsApp enabled number.

## Installation

1.  Clone the repository:

    ```bash
    git clone <repository_url>
    cd chatbot-immigration
    ```

2.  Create a virtual environment:

    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

## Configuration

1.  Set up your Twilio credentials:

    -   Replace `TWILIO_ACCOUNT_SID` and `TWILIO_AUTH_TOKEN` in [`application_3.py`](application_3.py) with your actual Twilio Account SID and Auth Token.
    -   Set the `twilio_number` to your Twilio WhatsApp number.

2.  Ensure Ollama is running and the Llama 3 model is accessible at `http://127.0.0.1:11434`.

## Running the Application

To start the Flask application, execute:

```bash
python application_3.py
