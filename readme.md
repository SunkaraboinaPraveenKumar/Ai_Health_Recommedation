```markdown
# Health Assistant Chatbot and Prediction Tool

This project is a full-stack web application designed to provide users with preliminary health information. It combines a symptom-based disease prediction tool with a conversational chatbot, all powered by machine learning models.

## Features

*   **Symptom-Based Disease Prediction:**
    *   Uses a Support Vector Classifier (SVC) model trained on a symptom dataset.
    *   Predicts potential diseases based on user-selected symptoms.
    *   Provides detailed information on predicted conditions, including descriptions, precautions, medications, and diet recommendations.
*   **Conversational Chatbot:**
    *   Employs a fine-tuned DistilGPT2 model for natural language interaction.
    *   Responds to user queries, offering preliminary insights into potential diseases, symptoms, and treatments based on text input.
*   **User-Friendly Interface:**
    *   Simple and intuitive interface for symptom selection and query input.
    *   Clear display of predictions, details, and chatbot responses.
*   **Backend API:**
    *   Built with Flask, handling routing, model interaction, and data processing.
    *   Handles data retrieval, processing and response.

## Technologies Used

*   **Backend:**
    *   Python 3.7+
    *   Flask
    *   `numpy`
    *   `pandas`
    *   `scikit-learn`
    *   `torch`
    *   `transformers`
    *   `pickle`
    *   `python-dotenv`
*   **Frontend:**
    *   HTML (Jinja2 templating)
    *   Basic CSS

## Setup and Installation

1.  **Clone the Repository:**

    ```bash
    git clone [YOUR_REPOSITORY_URL]
    cd health-assistant-app
    ```

2.  **Create a Virtual Environment:**

    ```bash
    python -m venv venv
    ```

    *   **Activate the virtual environment:**
        *   **Linux/macOS:**
            ```bash
            source venv/bin/activate
            ```
        *   **Windows:**
            ```bash
            venv\Scripts\activate
            ```

3.  **Install Dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

4.  **Set up Environment Variables:**
    *   Create a `.env` file in the root directory.
    *   Add your Hugging Face API token:

        ```env
        HUGGINGFACE_TOKEN=YOUR_HUGGINGFACE_API_TOKEN
        ```

5.  **Download the Required Models:**
    *   Make sure the `distilgpt2_finetuned.pth` and the `svc.pkl` files are present in their corresponding directories. These are essential for the application to work.

6. **Run the Application**

    ```bash
    python app.py
    ```
    The app will run on `http://127.0.0.1:5000/` by default

## Usage

1.  **Access the Application:**
    *   Open your web browser and go to `http://127.0.0.1:5000/` if running locally.

2.  **Disease Prediction:**
    *   On the homepage, select the symptoms you are experiencing from the available checkboxes.
    *   Click the "Predict Disease" button.
    *   The application will predict a potential disease and provide related information including description, precautions, medications, diet and workout recommendations.
    *   You may also search for the disease directly from the search bar.

3.  **Chatbot:**
    *   Navigate to the `/chatbot` route, or the appropriate link in the top navigation bar.
    *   Type your question or concern into the chatbot input field.
    *   The chatbot will respond with information about the disease, symptoms and treatments it was able to identify from the text.

## Project Structure

```
health-assistant-app/
├── app.py           # Main Flask application file
├── requirements.txt   # List of dependencies
├── .env               # Environment variables
├── templates/        # HTML template files
│   ├── index.html
│   ├── chatbot.html
│   ├── about.html
│   ├── contact.html
│   ├── blog.html
│   └── developer.html
├── datasets/         # CSV data files
│   ├── symptoms_df.csv
│   ├── precautions_df.csv
│   ├── workout_df.csv
│   ├── description.csv
│   ├── medications.csv
│   └── diets.csv
└── models/           # Saved model files
    ├── distilgpt2_finetuned.pth
    └── svc.pkl
```

## Contributing

If you'd like to contribute to this project, please follow these steps:

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/your-feature`).
3.  Make your changes and commit them (`git commit -m 'Add some feature'`).
4.  Push to the branch (`git push origin feature/your-feature`).
5.  Create a new pull request.

## License

This project is licensed under the [Your License Type] License - see the [LICENSE.md](LICENSE.md) file for details (replace with your license).

## Contact

If you have any questions, please feel free to contact me at [YOUR_EMAIL].
```

**Explanation of Key Parts:**

*   **Clear Heading:** The title is descriptive and informative.
*   **Concise Description:** Provides a brief overview of the application's purpose and capabilities.
*   **Features:** Uses bullet points to highlight key features of the application.
*   **Technologies Used:** Lists the major tools and technologies used in the project, categorized for clarity.
*   **Setup and Installation:** Provides step-by-step instructions, ensuring users can easily get started.
*   **Usage:** Gives a brief guide on how to interact with the application.
*   **Project Structure:** A tree structure that gives the user a look at how the project is laid out.
*   **Contributing:** Provides basic contribution guidelines.
*   **License:** Makes clear the project's license.
*   **Contact:** Encourages communication if there are any questions.

**How to Use This:**

1.  **Copy the Code:** Copy the entire Markdown code block.
2.  **Create a File:** Create a file named `README.md` in the root directory of your project.
3.  **Paste the Code:** Paste the code into the `README.md` file.
4.  **Customize:**
    *   Replace `[YOUR_REPOSITORY_URL]`, `YOUR_HUGGINGFACE_API_TOKEN`, `[Your License Type]`, and `[YOUR_EMAIL]` with your actual information.
    *   Add any additional instructions or sections as needed.
5.  **Save the File:** Save the changes to the `README.md` file.
6.  **Push to Repository:** Add, commit and push the file to your Git repository.

This `README.md` is well-formatted, informative, and helps potential users, collaborators, or future you understand the project. Remember to replace the bracketed placeholder information with your own details. Let me know if you have other questions!
