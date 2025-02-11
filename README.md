# AI Data Visualization Agent

## Overview

This Streamlit application provides an AI-powered data visualization agent that allows users to upload a CSV dataset and ask questions about it. The agent uses a large language model (LLM) from Together AI to generate responses and Python code to analyze the data and create visualizations, executed in a secure E2B (End-to-End Box) sandbox.

Live link: https://amishame24-ai-datavisualizat-ai-data-visualisation-agent-cmhrlr.streamlit.app/

## Features

*   **Interactive Data Exploration:**  Upload CSV files and explore the data with an interactive Streamlit interface.
*   **AI-Powered Analysis:**  Ask questions about your data in natural language, and the agent will generate Python code to answer them.
*   **Data Visualization:**  The agent can generate various types of visualizations based on the analysis, including charts and plots.
*   **Secure Code Execution:** Python code is executed in a sandboxed environment provided by E2B, ensuring security and isolation.
*   **Multiple LLM Support**: Choose from a selection of LLMs provided by Together AI
*   **Easy Setup**:  Simple installation process using `pip` and `requirements.txt`.

## Technologies Used

*   [Python](https://www.python.org/)
*   [Streamlit](https://streamlit.io/)
*   [Pandas](https://pandas.pydata.org/)
*   [Together AI](https://www.together.ai/)
*   [E2B (End-to-End Box)](https://e2b.dev/)
*   [Pillow (PIL Fork)](https://python-pillow.org/)

## Prerequisites

Before you begin, ensure you have met the following requirements:

*   **Python 3.7+:**  This project requires Python 3.7 or higher.
*   **Pip:**  Make sure you have pip installed.  It usually comes with Python.
*   **API Keys:**
    *   **Together AI API Key:**  Sign up for a free account at [Together AI](https://api.together.ai/signin) to get an API key.  Everyone gets a free \$1 credit.
    *   **E2B API Key:**  Sign up at [E2B](https://e2b.dev/) to obtain an API key.  Refer to the [E2B documentation](https://e2b.dev/docs/legacy/getting-started/api-key) for more information.

## Installation

1.  **Clone the repository:**

    ```
    git clone https://github.com/AmishaMe24/AI-DataVisualization-Agent
    cd AI-DataVisualization-Agent
    ```

2.  **Create a virtual environment (recommended):**

    ```
    python -m venv venv
    source venv/bin/activate  # On Linux/macOS
    venv\Scripts\activate  # On Windows
    ```

3.  **Install the dependencies:**

    ```
    pip install -r requirements.txt
    ```

## Setup

1.  **Set up API keys:**

    *   The application requires API keys for both Together AI and E2B.  You can provide these keys through the Streamlit sidebar.
    *   Alternatively (and recommended for security), set these as environment variables:

        *   Create a `.env` file in your project directory.
        *   Add the following lines to your `.env` file, replacing the placeholders with your actual keys:

            ```
            TOGETHER_API_KEY=YOUR_TOGETHER_AI_API_KEY
            E2B_API_KEY=YOUR_E2B_API_KEY
            ```

        *   Load the environment variables in your `main.py` file (or the main script) using `python-dotenv`:

            ```
            from dotenv import load_dotenv
            import os

            load_dotenv()
            together_api_key = os.getenv("TOGETHER_API_KEY")
            e2b_api_key = os.getenv("E2B_API_KEY")
            ```

## Usage

![chrome_8OYRQN6PQd](https://github.com/user-attachments/assets/ed26dbf3-cdd7-47e8-a6e3-bd6e71606a23)


1.  **Run the Streamlit application:**

    ```
    streamlit run main.py  # Or the name of your main script
    ```

2.  **Access the application:**  Open your web browser and go to the URL displayed in the terminal (usually `http://localhost:8501`).

3.  **Upload a CSV file:**  Use the file uploader to select a CSV file from your local machine.

4.  **Explore the dataset:**  View a preview of the data and toggle to show the full dataset.

5.  **Ask questions:**  Enter your query in the text area, describing what you want to know about the data.

6.  **Analyze:**  Click the "Analyze" button to submit your query to the AI agent.

7.  **View Results:** The application will display the LLM's response, any generated code, and any visualizations produced by the code.

## Example Queries

Here are a few example queries you can try:

*   "What is the average value of column X?"
*   "Create a bar chart showing the distribution of column Y."
*   "Compare the average cost for two people between different categories." (as in the original code)
*   "Show a scatter plot of column A vs. column B, colored by column C."

## Troubleshooting

*   **API Key Errors:**  If you encounter errors related to API keys, double-check that you have entered the correct keys in the sidebar or set them as environment variables.
*   **Package Import Errors:** If you get errors about missing modules, ensure that you have activated your virtual environment (if using one) and that all dependencies are installed from `requirements.txt`.
*   **E2B Sandbox Issues:**  If you encounter issues with the E2B sandbox, consult the [E2B documentation](https://e2b.dev/docs/legacy).
*   **Model Load Errors:** If the model does not load, ensure that you have a stable internet connection and that the model name is correctly specified in the sidebar.

## Contributing

Contributions are welcome!  If you find a bug or have an idea for a new feature, please open an issue or submit a pull request.

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Make your changes.
4.  Submit a pull request.

