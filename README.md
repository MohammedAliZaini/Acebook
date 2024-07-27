# Acebook

**Team Watermelon 🍉**

In this project, we worked on an existing application, focusing on familiarising ourselves with the inherited codebase to improve and extend its functionality.

## Team Members

- Benedict Hall
- Jet Siva
- Jose Lopez
- Mohammed Ali Zaini
- Oluwatomi Taiwo
- Xiangnan Liu

## Project Structure

This repository contains two main applications:

1. **Frontend** - A React application
2. **Backend** - An API server

These applications communicate via HTTP requests and must be run separately.

## Documentation

For detailed documentation on the codebase and its architecture, refer to the following resources:

- [Card Wall](https://trello.com/invite/b/CAG0mne5/ATTI46bc65d94a96bf646d1ba0b0c8ed00a1321F2CD7/acebook-watermelon)

## Quickstart

### Install Node.js

1. Ensure Node.js and Node Version Manager (NVM) are installed.

2. Install NVM using Homebrew:

    ```bash
    brew install nvm
    ```

   Follow the instructions to update your `~/.bash_profile`. Open a new terminal and install the latest version of Node.js:

    ```bash
    nvm install 20
    ```

### Set Up the Project

1. Fork this repository and rename the fork to `acebook-<team-name>`.

2. Clone the fork to your local machine.

3. Install dependencies for both frontend and API applications:

    ```bash
    cd frontend
    npm install
    cd ../api
    npm install
    ```

4. Install an ESLint plugin for your editor (e.g., ESLint for VSCode).

### Install MongoDB

1. Install MongoDB using Homebrew:

    ```bash
    brew tap mongodb/brew
    brew install mongodb-community@6.0
    ```

   If prompted to add MongoDB to your PATH, follow the instructions and restart your terminal.

2. Start MongoDB:

    ```bash
    brew services start mongodb-community@6.0
    ```

### Configure Environment Variables

Create `.env` files in both the frontend and backend directories.

**Frontend:**

Create `frontend/.env` with the following content:

    ```env
    VITE_BACKEND_URL="http://localhost:3000"
    ```

**Backend:**

Create `api/.env` with the following content:

    ```env
    MONGODB_URL="mongodb://0.0.0.0/acebook"
    NODE_ENV="development"
    JWT_SECRET="secret"
    ```

For detailed explanations of these environment variables, refer to the documentation.

### Run the Application

1. Start the backend server (in the `api` directory) in development mode:

    ```bash
    cd api
    npm run dev
    ```

2. Start the frontend application (in the `frontend` directory):

    ```bash
    cd frontend
    npm run dev
    ```

3. Open your browser and navigate to `http://localhost:5174/signup` to create a new user.

4. After signing up, log in by going to `http://localhost:5174/login`.

   Note: After logging in, you might not see much initially, but you can create posts using Postman, which will appear in the browser upon refreshing the page.
