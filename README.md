# Email Analyzer

Email Analyzer is a web application that uses Ollama with LLaMA or Mistral models to analyze sales emails for professionalism and effectiveness. It provides a comprehensive evaluation of various aspects of the email, helping sales professionals improve their email communication.

## Features

- Analyzes sales emails for tone, clarity, structure, and effectiveness
- Provides detailed feedback on multiple aspects of the email
- Simple and intuitive web interface
- Powered by Ollama with LLaMA or Mistral models

## Requirements

- Python 3.7+
- Flask
- Requests library
- Ollama installed and running locally

## Setup

1. Clone the repository or download the source code:
   ```
   git clone https://github.com/desirit/email-analyzer.git
   cd email-analyzer
   ```

2. It's recommended to create a virtual environment:
   ```
   python3 -m venv venv  # Make sure to use Python 3 and not Python 2.7
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install the required Python packages using the `requirements.txt` file:
   ```
   pip install -r requirements.txt
   ```

4. Install Ollama by following the instructions at [Ollama's official website](https://ollama.ai/).

5. Pull the LLaMA2 or Mistral model using Ollama:
   ```
   ollama pull llama2
   # or
   ollama pull mistral
   ```

6. Start the Ollama server:
   ```
   ollama serve
   ```

## Running the Application

1. Ensure you're in the project directory and your virtual environment is activated.

2. Make sure the Ollama server is running.

3. Run the Flask application:
   ```
   python app.py
   ```

4. Open a web browser and go to `http://localhost:5000` to access the application.

## Usage

1. On the home page, you'll see a text area where you can paste your sales email content.

2. Click the "Analyze" button to submit the email for analysis.

3. The application will send the email to the Ollama API for processing and display the results on a new page.

4. The analysis will cover the following aspects of your email:
   - Overall Impression
   - Tone and Professionalism
   - Clarity and Coherence
   - Structure and Organization
   - Opening and Closing
   - Call-to-Action
   - Personalization
   - Grammar and Spelling
   - Length and Conciseness
   - Suggestions for Improvement

5. Review the analysis and use the feedback to improve your email.

6. Click "Analyze Another Email" to return to the home page and analyze another email.

## Customization

You can modify the `app.py` file to customize the application:

- Adjust the HTML templates to change the appearance of the web pages.
- Modify the prompt in the `analyze_email()` function to change the aspects of the email being analyzed.
- Change the Ollama model by modifying the `MODEL_NAME` variable (e.g., "llama2" or "mistral").

## Security Note

This application is a basic example and may not be suitable for production use without additional security measures. Ensure you implement proper security practices, such as input validation and protection against common web vulnerabilities, before deploying this application in a production environment.

## License

This project is open-source and available under the MIT License.

## Acknowledgments

This application uses Ollama with LLaMA or Mistral models to provide AI-powered email analysis.
