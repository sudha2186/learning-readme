# CS50 MESSENGER
#### Video Demo:  https://youtu.be/lK3h4tbaW5A
#### Description:
# Messenger Web Application

A web-based messenger built using **HTML**, **CSS**, **Flask**, and **SQL**. This application that I built as part of my CS50 course project. This platform allows users to register, log in, send messages, reply to messages, and manage their inbox effectively.

## Features

- User authentication (Login/Register).
- Real-time messaging between users.
- Display message history for each user.
- Responsive design for desktop and mobile devices.
- Simple and intuitive user interface.
- Able to Reply and Delete the message in UI

## Technologies Used

- **Frontend**: HTML, CSS
- **Backend**: Flask (Python)
- **Database**: SQL (SQLite for development, MySQL in production)
- **Libraries**:
  - <ins>cs50</ins>: To access some libraries directly
  - <ins>Flask</ins>: To build web applications and APIs.
  - <ins>Flask-Session</ins>: To manage server-side sessions (storing session data on the server).
  - <ins>pytz</ins>: To manage server-side sessions (storing session data on the server).
  - <ins>requests</ins>: To make HTTP requests to external services or APIs.

## Installation

Before running the application, make sure you have the following installed:
- Python 3.7 or higher
- pip (Python package installer)

### STEP 1: Install the dependencies
- pip install -r requirements.txt
- pip install flask

### Step 2: Set up the database
- sqlite3 `project.db`

### Step 3: Run the application
- flask run

## Flask Code

- `app.py`
- `helpers.py`

## Features Implemented

### 1. User Registration and Login

  - **What I Did**:
      - Created a user authentication system using Flask sessions.
      - Passwords are securely stored in the database after hashing.
      - User registration requires a unique username, and optional email and phone number fields are available.
      - During login, the system verifies user credentials and initiates a session.

  - **Challenges**:

      - Implementing secure password storage and validation.
      - Managing sessions to prevent unauthorized access.

### 2. Inbox Management

  - What I Did:
      - Built a feature to display messages in an inbox format.
      - Added sender and receiver details with dynamic labeling.
      - Displayed the message subject, body (truncated for simplicity), timestamp, and message status.

  - Challenges:

      - Querying the database efficiently to fetch only relevant messages for the logged-in user.

### 3. Reply Functionality

  - **What I Did**:
      - Developed a reply feature that pre-fills the recipient field with the sender's username.
      - Included input validation to ensure valid recipients exist in the database.
      - Integrated a form for replying to messages directly from the inbox.

  - **Challenges**:

      - Ensuring the sender and receiver fields were properly maintained.

### 4. Message Deletion and Trash Management

  - **What I Did**:
      - Created a "Trash" feature where deleted messages are moved rather than permanently deleted.
      - Messages marked as deleted are hidden from the main inbox and displayed in a separate trash page.
      - Added options to restore or permanently delete messages from the trash.

  - **Challenges**:

      - Updating the database schema to handle soft deletions using a deleted flag.
      - Managing message visibility across inbox and trash views.

### 5. Database Design

  - **What I Did**:
      - Designed the database with three primary tables:
      - users: Stores user information, including hashed passwords.
      - messages: Stores messages with sender and receiver references.
      - contacts: Manages all the sender and receiver of registered user.
      - Used SQL queries to fetch messages dynamically based on the user's ID.

  - **Challenges**:

      - Designing efficient queries to fetch only relevant messages.
      - Maintaining relational integrity between the users,contacts and messages tables.

### 6. User Interface

  - **What I Did**:
      - Used HTML and Bootstrap for a clean, responsive design.
      - Designed pages for login, registration, inbox, trash, and reply functionality.
      - messages: Stores messages with sender and receiver references.
      - Ensured the interface is user-friendly and mobile-compatible.

  - **Challenges**:

      - Styling dynamic elements like message tables.
      - Maintaining consistent design across pages.

## What’s Next?

- Add a real-time messaging feature using WebSockets.
- Implement a search bar for finding messages by subject or user.

## Key Learnings

- Implementing user authentication securely with Flask sessions.
- Designing relational databases for message management.
- Debugging dynamic content rendering with template engines like Jinja2.
- Creating a responsive UI using Bootstrap.

## Acknowledgments
This project is part of my CS50 coursework. Special thanks to the CS50 teaching team for the guidance and support.
