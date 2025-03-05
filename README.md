# LangChain: Chat with SQL Database

## Overview
This is a Streamlit-based application that enables users to interact with an SQL database using natural language queries powered by LangChain and the Groq API. The application supports both SQLite and MySQL databases.

## Features
- Chat interface for querying an SQL database.
- Supports SQLite (`student.db`) and MySQL databases.
- Uses LangChain's SQL agent to process queries.
- Integrates with Groq API for LLM-based responses.
- Maintains conversation history within the session.
- Securely inputs MySQL credentials and Groq API key through the sidebar.

## Requirements
- Python 3.8+
- Streamlit
- LangChain
- SQLAlchemy
- SQLite3
- MySQL Connector (if using MySQL)
- Groq API Key

## Installation
1. Clone this repository:
   ```bash
   git clone <repo-url>
   cd <repo-folder>
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```
2. Select the database type in the sidebar:
   - **SQLite:** Uses `student.db`
   - **MySQL:** Requires hostname, username, password, and database name
3. Enter the Groq API key in the sidebar.
4. Start chatting with your database!

## Configuration
- **SQLite Database:** Ensure `student.db` is located in the same directory as `app.py`.
- **MySQL Database:** Provide valid MySQL credentials in the sidebar.
- **Groq API Key:** Required to interact with the LLM.

## File Structure
```
├── app.py                # Main application file
├── student.db            # Sample SQLite database (if using SQLite)
├── requirements.txt      # Required dependencies
```

## Notes
- Query execution is handled using LangChain’s SQL agent.
- The app uses Streamlit's session state to manage conversation history.
- Caching is used to optimize database connections.

## License
This project is open-source under the MIT License.

