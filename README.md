# SQL-Powered Chat Application
This project is a Streamlit-based chat application that integrates with a SQL database, using OpenAI's GPT model for natural language processing and LangChain utilities for querying and processing data. The application allows users to ask questions in natural language, fetches relevant data from an SQL database, and provides intelligent answers.

# Features

Natural Language Querying: Users can ask questions in plain English, and the application converts them into SQL queries.

Dynamic Table Selection: Automatically selects relevant database tables based on user queries.

Integration with GPT-4: Uses OpenAI's GPT-4 for generating SQL queries and interpreting results.

Streamlit Interface: Provides an intuitive chat interface for seamless interaction.

History Management: Maintains a session-based history of user and assistant messages.

# Prerequisites

Python 3.8 or later.

OpenAI API key.

SQL Server with appropriate credentials.

# Setup Instructions

### Clone the Repository
   
   git clone <REPO_URL>

   cd <REPO_NAME>


### Configure Environment Variables

Set the following environment variables:

OPENAI_API_KEY: Your OpenAI API key.

LANGCHAIN_TRACING_V2: Set to 'true'.

LANGCHAIN_ENDPOINT: Set to https://api.smith.langchain.com.

### Create Database

Create a database in SQL server with the data you would like to use.

### Database Configuration

Update the following database connection details in the code:

server: Replace <DATABASE_SERVER_NAME> with your SQL server name.

database: Replace <DATABASE_NAME> with your SQL server database name.

username: Replace <USER_NAME> with your SQL username.

password: Replace <DATABASE_PASSWORD> with your SQL password.

driver: Ensure ODBC Driver 17 for SQL Server is installed.

### Prepare Table Details

Create a table_details.csv file in the project directory with the following format:

Table,Description

table_name_1,Description of table_name_1

table_name_2,Description of table_name_2

# Running the Application

Start the application with the following command:

streamlit run nlToSql.py

# Application Flow

User Interaction: Users ask questions via the chat interface.

Table Selection: The app dynamically identifies relevant SQL tables using OpenAI.

SQL Query Generation: Generates and executes SQL queries based on the user's question.

Response Delivery: Formats and presents query results in the chat interface.

# Project Structure

nlToSql.py: Main application script.

table_details.csv: Metadata file for SQL tables.

# Key libraries used in the project:

Streamlit: For building the chat interface.

LangChain: For managing LLMs and database querying.

SQLAlchemy: For connecting to the SQL database.

OpenAI: For GPT-powered natural language processing.

Pandas: For processing table metadata.

# Future Improvements

Add support for multiple database types.

Improve error handling for invalid queries.

Enhance table relevance scoring for complex queries.
