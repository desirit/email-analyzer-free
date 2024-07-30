# Email Analyzer

Email Analyzer is a user-friendly web application that helps you improve your sales emails. It analyzes your emails for professionalism and effectiveness, providing detailed feedback on various aspects of your writing.

## What You'll Need

Before you start, make sure you have the following software installed on your computer:

1. **Git**: This helps you download the project files.
   - Download from: https://git-scm.com/downloads
   - Installation guide: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

2. **Python 3**: This is the programming language the application uses.
   - Download from: https://www.python.org/downloads/
   - Choose Python 3.7 or later
   - Installation guide: https://wiki.python.org/moin/BeginnersGuide/Download

3. **Ollama**: This runs the AI model that analyzes your emails.
   - Download from: https://ollama.ai/download
   - Follow the installation instructions on the website

## Setting Up the Application

Follow these steps to set up the Email Analyzer on your computer:

1. Open a command prompt or terminal on your computer.

2. Download the project files:
   ```
   git clone https://github.com/yourusername/email-analyzer.git
   ```

3. Navigate to the project folder:
   ```
   cd email-analyzer
   ```

4. Create a virtual environment (this keeps the project separate from other Python projects):
   - On Windows:
     ```
     python -m venv venv
     venv\Scripts\activate
     ```
   - On macOS or Linux:
     ```
     python3 -m venv venv
     source venv/bin/activate
     ```

5. Install the required Python packages:
   ```
   pip install -r requirements.txt
   ```

6. Download the AI model:
   ```
   ollama pull llama2
   ```

## Running the Application

You'll need to use two separate command prompt or terminal windows:

### Window 1: Starting Ollama

1. Open a new command prompt or terminal window.
2. Start the Ollama server:
   ```
   ollama serve
   ```
3. Keep this window open and running.

### Window 2: Running the Email Analyzer

1. Open another command prompt or terminal window.
2. Navigate to your project folder (if you're not already there):
   ```
   cd path/to/email-analyzer
   ```
3. Activate the virtual environment:
   - On Windows:
     ```
     venv\Scripts\activate
     ```
   - On macOS or Linux:
     ```
     source venv/bin/activate
     ```
4. Run the Flask application:
   ```
   python app.py
   ```
5. You should see a message saying the server is running.

## Using the Email Analyzer

1. Open a web browser and go to `http://localhost:5000`
2. You'll see a text box where you can paste your sales email.
3. Click the "Analyze" button to submit your email for analysis.
4. Wait a few moments for the AI to analyze your email.
5. Review the feedback provided, covering aspects like tone, clarity, and structure.
6. Use the suggestions to improve your email.

## Customization

If you're comfortable with coding, you can modify the `app.py` file to customize the application:

- Change the appearance by editing the HTML templates.
- Modify the analysis criteria by adjusting the prompt in the `analyze_email()` function.
- Switch to a different AI model by changing the `MODEL_NAME` variable (e.g., from "llama2" to "mistral").

## Troubleshooting

If you encounter any issues:
1. Make sure both Ollama and the Flask application are running in separate windows.
2. Check that you've installed all required software and followed the setup steps.
3. Try restarting both Ollama and the Flask application.

If problems persist, feel free to open an issue on the GitHub repository.

## Security Note

This application is a basic example and may not be suitable for sensitive or confidential information. Use it responsibly and avoid sharing private data.

## License

This project is open-source and available under the MIT License.

## Acknowledgments

This application uses Ollama with the LLaMA model to provide AI-powered email analysis.
