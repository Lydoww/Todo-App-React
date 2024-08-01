# Todo-App

Welcome to the Todo-App project! This is a task management application built with React for the frontend and Node.js / PostgreSQL for the backend. Follow the instructions below to set up and run the application locally.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (includes npm)
- [PostgreSQL](https://www.postgresql.org/download/)(PSQL)
- [Visual Studio Code](https://code.visualstudio.com/) (VS Code)

## Installation

The project is divided into two parts: the client and the server. You need to set them up separately.

### Server Setup

1. **Create a `.env` file** at the root of the server directory and configure it with your database and server information. Below is an example configuration:

    ```env
    USERNAME=test
    PASSWORD=test
    HOST=localhost
    DBPORT=5432
    ```

2. **PostgreSQL Database Setup**

   Follow the steps below to set up your PostgreSQL database:

   - **Access the PostgreSQL Interface (this is a linux installation):**

     ```bash
     sudo -i -u postgres psql
     ```

   - **Create a New User and Database:**

     ```sql
     CREATE USER username WITH PASSWORD 'yourpassword';
     CREATE DATABASE dbname OWNER username;
     ```

   - **Disconnect from `psql`:**

     Press `Ctrl + D`.

   - **Test the Database Connection:**

     ```bash
     psql -U username -d dbname
     ```

   - **Execute an SQL Script:**

     ```bash
     psql -U username -d dbname -f path/to/file.sql
     ```

### 3. Update the Database Name in `db.js`

Once you have completed the previous steps, you need to configure your database connection. Open the `db.js` file and update the database name with the name you used during the PostgreSQL setup.

### Client Setup

1. **Navigate to the `client` directory:**

    ```bash
    cd client
    ```

2. **Install the necessary dependencies:**

    ```bash
    npm install
    ```

3. **Create a `.env` file** in the client root and add the following configuration:

    ```env
    REACT_APP_SERVERURL=http://localhost:8000
    ```

4. **Start the client application:**

    ```bash
    npm start
    ```

    The client application will be available at [http://localhost:3000](http://localhost:3000).

### Server

1. **Navigate to the `server` directory:**

    ```bash
    cd server
    ```

2. **Install the necessary dependencies:**

    ```bash
    npm install
    ```

3. **Start the server:**

    ```bash
    npm start
    ```

    The server will be available at [http://localhost:8000](http://localhost:8000).

### Usage

1. **Create an Account:**

   - You will land on the login page. Click on the "Sign Up" button to create a new account.
   - Fill in the required information and complete the registration process (e.g., `lydoww@test.com` / `123`).

2. **Log In:**

   - After creating an account, use the "Log In" button to access the application.
   - Enter the email and password you used during the sign-up process.

Enjoy using the Todo-App!
