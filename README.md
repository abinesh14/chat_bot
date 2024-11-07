<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chat with Gemini-Pro! - Chatbot Application</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 0;
            color: #333;
        }

        .container {
            width: 80%;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
        }

        h1 {
            text-align: center;
            color: #007BFF;
        }

        h2 {
            color: #333;
        }

        ul {
            line-height: 1.6;
            padding-left: 20px;
        }

        .section {
            margin-bottom: 30px;
        }

        .code-block {
            background-color: #f2f2f2;
            padding: 15px;
            border-radius: 8px;
            font-family: "Courier New", Courier, monospace;
            color: #333;
            margin-top: 10px;
            white-space: pre-wrap;
            word-wrap: break-word;
        }

        .note {
            background-color: #fff3cd;
            padding: 10px;
            border-radius: 8px;
            border: 1px solid #ffeeba;
            color: #856404;
            margin-top: 10px;
        }

        footer {
            text-align: center;
            padding: 20px;
            background-color: #007BFF;
            color: #fff;
            margin-top: 30px;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Chat with Gemini-Pro! - Chatbot Application</h1>

        <div class="section">
            <h2>Overview</h2>
            <p>This is a chatbot application built using <strong>Streamlit</strong> and the <strong>Google Gemini-Pro AI model</strong> (specifically the <code>gemini-1.5-flash</code> variant). Users can interact with the chatbot in a conversational interface, where the bot responds to user queries.</p>
        </div>

        <div class="section">
            <h2>Features</h2>
            <ul>
                <li><strong>Conversational Chat Interface</strong>: Users can chat with the Gemini-Pro AI model, which provides intelligent responses.</li>
                <li><strong>Chat History</strong>: The application stores and displays the history of interactions between the user and the chatbot.</li>
                <li><strong>Easy Deployment</strong>: The app is designed to be easily deployable with Streamlit, allowing you to run it as a web app.</li>
                <li><strong>API Integration</strong>: It integrates with Google’s Gemini-Pro API for generating responses.</li>
            </ul>
        </div>

        <div class="section">
            <h2>Requirements</h2>
            <p>Before running the application, make sure to install the following dependencies:</p>
            <ul>
                <li><strong>Streamlit</strong>: For creating the web-based interface.</li>
                <li><strong>Google Generative AI</strong>: For integrating with the Gemini-Pro model.</li>
            </ul>
        </div>

        <div class="section">
            <h2>Installation</h2>
            <p>Follow these steps to set up the application:</p>
            <ol>
                <li>Clone or download the project to your local machine.</li>
                <li>Set up a virtual environment (optional but recommended):</li>
                <div class="code-block">
                    python -m venv myenv<br>
                    source myenv/bin/activate  <!-- For macOS/Linux --> <br>
                    myenv\Scripts\activate     <!-- For Windows -->
                </div>
                <li>Install the required libraries:</li>
                <div class="code-block">
                    pip install streamlit google-generativeai
                </div>
                <li>Get your <strong>Google API Key</strong> for the Gemini-Pro model and replace it in the <code>GOOGLE_API_KEY</code> variable in the <code>app.py</code> file.</li>
            </ol>
        </div>

        <div class="section">
            <h2>Running the Application</h2>
            <p>Once the dependencies are installed and your API key is configured, run the application using:</p>
            <div class="code-block">
                streamlit run app.py
            </div>
            <p>Open your browser and visit the local address displayed in the terminal (usually <code>http://localhost:8501</code>), where the chatbot interface will be available.</p>
        </div>

        <div class="section">
            <h2>How It Works</h2>
            <p>The application uses Streamlit to create the user interface with a chat window. It displays previous messages and allows users to input new prompts. When the user submits a prompt, it is sent to the Gemini-Pro model, and the bot’s response is displayed in the chat window. The chat history is maintained using <code>st.session_state</code>.</p>
        </div>

        <div class="section">
            <h2>Key Files</h2>
            <ul>
                <li><strong>app.py</strong>: Main application file containing all the code to run the chatbot.</li>
                <li><strong>requirements.txt</strong>: List of required Python libraries for the project.</li>
            </ul>
        </div>

        <div class="section">
            <h2>How to Customize</h2>
            <ul>
                <li><strong>Change the Model</strong>: If you want to use a different model variant, modify the <code>gemini-1.5-flash</code> value in the <code>model = gen_ai.GenerativeModel("gemini-1.5-flash")</code> line.</li>
                <li><strong>UI Customization</strong>: You can adjust the page layout and design by changing the Streamlit settings in <code>st.set_page_config</code>.</li>
                <li><strong>Enhance Functionality</strong>: You can further enhance the chatbot by adding more features like sentiment analysis, multi-language support, or even a database to store user interactions.</li>
            </ul>
        </div>

        <div class="note">
            <strong>Note:</strong> Ensure that your API key is correctly set and that you have the necessary permissions to use the Google Gemini-Pro model.
        </div>

        <footer>
            <p>© 2024 Chat with Gemini-Pro. All rights reserved.</p>
        </footer>
    </div>

</body>
</html>
