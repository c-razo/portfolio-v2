### **Ticketing System Project**

#### **Project Overview**
This is a fully-functional ticketing system built with Flask and SQLite, featuring user authentication using JWT (JSON Web Tokens). The system allows users to register, log in, submit support tickets, and view the status of their tickets. It's designed to help manage support requests in an intuitive and secure manner.

#### **Technologies Used**
- **Backend**: Python, Flask
- **Database**: SQLite
- **Authentication**: JWT (JSON Web Tokens)
- **Frontend**: HTML, CSS (via templates in Flask)

#### **Features**
- **User Registration**: Allows new users to create an account.
- **User Login**: Provides a login system where users can authenticate via email and password.
- **Ticket Submission**: Authenticated users can submit new tickets, which are stored in the database.
- **Ticket Viewing**: Users can view a list of their tickets and their statuses.
- **Ticket Resolution**: Agents can mark tickets as resolved.

#### **Installation Instructions**
1. **Clone the repository:**
    ```bash
    git clone https://github.com/c-razo/ticketing-system.git
    cd ticketing-system
    ```
2. **Set up a virtual environment:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On macOS/Linux
    venv\Scripts\activate     # On Windows
    ```
3. **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
4. **Run the application:**
    ```bash
    python backend/app.py
    ```
5. **Navigate to** `http://127.0.0.1:5000` in your browser to access the app.

#### **Screenshots**
- **Login Page**  
   ![Login Page](https://raw.githubusercontent.com/c-razo/ticketing-system/main/assets/login.png)
- **Tickets Page**  
   ![Tickets Page](https://raw.githubusercontent.com/c-razo/ticketing-system/main/assets/tickets.png)

#### **Demo**
Check out the live demo on [Heroku](https://ticketing-system-demo-6fe8ff4c2d74.herokuapp.com) or [GitHub Pages](https://github.com/c-razo/ticketing-system) for a quick preview (if applicable).

#### **Challenges**
- Implementing JWT authentication securely
- Handling user sessions in a stateless environment
- Managing and tracking ticket statuses

#### **Future Improvements**
- Add email notifications for ticket updates
- Integrate with an external ticketing platform for advanced features
- Add an admin panel for agents to manage tickets more efficiently
