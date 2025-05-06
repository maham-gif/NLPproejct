

AUST University Advisor Chatbot

Description
This is a Flask-based AI chatbot designed for students of AUST to get automated responses to frequently asked university-related queries. The chatbot reads questions and answers from a cleaned Excel dataset containing multiple sheets. If the bot cannot find a close match for a question, it classifies the query into one of five predefined domains and assigns it to a corresponding teacher for manual input. Once a teacher provides the answer, it is saved into the dataset for future use.

Features

* Rule-based classification of questions into five domains: Admission, Scholarship, Student Affairs, Academics, Migration
* Each domain is linked to a specific faculty member for manual query handling
* Intelligent matching of student queries using fuzzy string matching
* Integration of common chatbot greetings and responses
* Dynamic update of the dataset when a teacher answers a new question
* Unread message count for teachers to track pending queries
* Separate user and teacher interfaces
* Session-based storage of recent chatbot responses

Technologies Used

* Python 3
* Flask
* Pandas
* OpenPyXL
* HTML, CSS (Embedded via render\_template\_string)

Project Structure

* main.py (Flask application with chatbot and teacher routes)
* DATASET\_CLEANED.xlsx (Excel file containing Q\&A in Sheet1, Sheet2, Sheet3)

How It Works

1. User asks a question on the chatbot interface.
2. The app first checks if the question matches a common greeting.
3. If not found, it checks the Excel dataset using fuzzy matching.
4. If no close match is found, the query is classified based on keywords.
5. The query is assigned to a teacher of the relevant domain, and the teacher interface is displayed.
6. Teacher submits an appropriate answer.
7. The new Q\&A pair is appended to Sheet1 of the dataset and stored in memory.
8. The chatbot learns and answers future similar questions without manual help.

How to Run

1. Ensure Python 3 is installed.
2. Install required libraries using:
   pip install flask pandas openpyxl
3. Place the dataset file (DATASET\_CLEANED.xlsx) in the specified path or update the path in the code.
4. Run the Flask app:
   python main.py
5. Access the chatbot in your browser at:
   [http://localhost:5000](http://localhost:5000)

Future Improvements

* Add authentication for teachers
* Include more advanced NLP-based classification
* Log user sessions and query history
* Integrate notifications (e.g., email or SMS) to alert teachers of new queries
* Enable multi-language support

Credits
Developed as a university final year project to assist students at AUST with academic and administrative queries using AI and automation.


