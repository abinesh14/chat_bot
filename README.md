<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Chat with Gemini-Pro! - Chatbot Application</title>
</head>
<body>
    <h1>Chat with Gemini-Pro! - Chatbot Application</h1>

    <p>This is a chatbot application built using <strong>Streamlit</strong> and the <strong>Google Gemini-Pro AI</strong> model (specifically the <code>gemini-1.5-flash</code> variant). Users can interact with the chatbot in a conversational interface, where the bot responds to user queries.</p>

    <h2>Features</h2>
    <ul>
        <li><strong>Conversational Chat Interface</strong>: Users can chat with the Gemini-Pro AI model, which provides intelligent responses.</li>
        <li><strong>Chat History</strong>: The application stores and displays the history of interactions between the user and the chatbot.</li>
        <li><strong>Easy Deployment</strong>: The app is designed to be easily deployable with Streamlit, allowing you to run it as a web app.</li>
        <li><strong>API Integration</strong>: It integrates with Google’s Gemini-Pro API for generating responses.</li>
    </ul>

    <h2>Requirements</h2>
    <p>Before running the application, make sure to install the following dependencies:</p>
    <ul>
        <li><strong>Streamlit</strong>: For creating the web-based interface.</li>
        <li><strong>Google Generative AI</strong>: For integrating with the Gemini-Pro model.</li>
    </ul>

    <h3>Installation</h3>
    <ol>
        <li>Clone or download the project to your local machine.</li>
        <li>Set up a virtual environment (optional but recommended):
            <pre><code>python -m venv myenv</code></pre>
            For macOS/Linux:
            <pre><code>source myenv/bin/activate</code></pre>
            For Windows:
            <pre><code>myenv\Scripts\activate</code></pre>
        </li>
        <li>Install the required libraries:
            <pre><code>pip install streamlit google-generativeai</code></pre>
        </li>
        <li>Get your <strong>Google API Key</strong> for the Gemini-Pro model and replace it in the <code>GOOGLE_API_KEY</code> variable in the <code>app.py</code> file.</li>
    </ol>

    <h2>Running the Application</h2>
    <ol>
        <li>After installing the dependencies and configuring the API key, run the application using:
            <pre><code>streamlit run app.py</code></pre>
        </li>
        <li>Open your browser and visit the local address displayed in the terminal (usually <code>http://localhost:8501</code>), where the chatbot interface will be available.</li>
    </ol>

    <h2>How It Works</h2>
    <ul>
        <li><strong>Streamlit Interface</strong>: The application uses Streamlit to create the user interface with a chat window. It displays previous messages and allows users to input new prompts.</li>
        <li><strong>API Key Configuration</strong>: The application uses Google’s Gemini-Pro model via the <code>google.generativeai</code> library. The API key is directly embedded into the script for authentication.</li>
        <li><strong>Chat History Management</strong>: The chat history is maintained in <code>st.session_state</code>, ensuring that the chat persists during the user session.</li>
        <li><strong>Interaction</strong>: Users can type their queries in the provided input field. Upon submission, the query is sent to the Gemini-Pro model, and the model’s response is displayed in the chat window.</li>
    </ul>

    <h2>Key Files</h2>
    <ul>
        <li><strong>app.py</strong>: Main application file containing all the code to run the chatbot.</li>
        <li><strong>requirements.txt</strong>: List of required Python libraries for the project.</li>
    </ul>

    <h2>How to Customize</h2>
    <ul>
        <li><strong>Change the Model</strong>: If you want to use a different model variant, modify the <code>gemini-1.5-flash</code> value in the <code>model = gen_ai.GenerativeModel("gemini-1.5-flash")</code> line.</li>
        <li><strong>UI Customization</strong>: You can adjust the page layout and design by changing the Streamlit settings in <code>st.set_page_config</code>.</li>
        <li><strong>Enhance Functionality</strong>: You can further enhance the chatbot by adding more features like sentiment analysis, multi-language support, or even a database to store user interactions.</li>
    </ul>

    <h2>Troubleshooting</h2>
    <ul>
        <li><strong>API Key Issues</strong>: If you encounter issues with the API key, ensure that your Google API key is correctly set and that you have the necessary permissions.</li>
        <li><strong>Streamlit Issues</strong>: If Streamlit doesn’t open the app properly, try clearing the cache by running <code>streamlit cache clear</code>.</li>
    </ul>

    <h2>License</h2>
    <p>This project is licensed under the MIT License.</p>
</body>
</html>
