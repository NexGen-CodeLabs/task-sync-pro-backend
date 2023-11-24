# TaskSync Pro Backend

TaskSync Pro Backend is the server-side component of the real-time collaborative task management application. It is built with Node.js and Express, utilizing MongoDB as the database through Mongoose.

## Table of Contents
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- [Environment Variables](#environment-variables)
- [Contributing](#contributing)
- [License](#license)

## Getting Started

### Prerequisites
- Node.js and npm installed. [Download and install Node.js](https://nodejs.org/)
- MongoDB installed and running. [Download and install MongoDB](https://www.mongodb.com/try/download/community)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/NexGen-CodeLabs/task-sync-pro-backend.git
   cd task-sync-pro-backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up your environment variables:
   - Create a `.env` file based on the provided `.env.example`.
   - Configure the variables with your MongoDB connection URI and any other required settings.

4. Start the server:
   ```bash
   npm start
   ```

   The server will be available at `http://localhost:3001/` by default.

## Project Structure

The project follows a structured organization to enhance maintainability and scalability. Here's an overview of the file structure:

```
task-sync-pro-backend/
|-- config/
|-- controllers/
|-- middleware/
|-- models/
|-- routes/
|-- utils/
|-- app.js
|-- server.js
|-- .gitignore
|-- package.json
|-- README.md
|-- .env.example
```

- **config/:** Configuration files, including database configuration (`database.js`) and a general configuration file (`index.js`).

- **controllers/:** Controllers responsible for handling different aspects of the application logic.

- **middleware/:** Custom middleware functions.

- **models/:** Mongoose models defining the structure of documents in the MongoDB database.

- **routes/:** Express.js route definitions.

- **utils/:** Utility functions shared across the application.

- **app.js:** The main application file where middleware and routes are configured.

- **server.js:** The entry point of the server.

- **.gitignore:** Specifies files and directories to be ignored by version control.

- **package.json:** Configuration file for npm.

- **README.md:** Documentation for the backend, including setup instructions and any other relevant information.

- **.env.example:** An example environment variable file.

## API Endpoints

- **Authentication:**
  - `POST /api/auth/signup`: Register a new user.
  - `POST /api/auth/login`: Log in a user.

- **Task Management:**
  - `GET /api/tasks`: Get all tasks.
  - `POST /api/tasks`: Create a new task.
  - `GET /api/tasks/:taskId`: Get details of a specific task.
  - `PUT /api/tasks/:taskId`: Update a task.
  - `DELETE /api/tasks/:taskId`: Delete a task.

For detailed API documentation, refer to the [API documentation](API_DOCUMENTATION.md).

## Environment Variables

- `PORT`: The port on which the server will run.
- `MONGODB_URI`: The MongoDB connection URI.

## Contributing

Contributions are welcome! If you'd like to contribute to TaskSync Pro Backend, please follow our [contribution guidelines](CONTRIBUTING.md).

## License

This project is licensed under the [MIT License](LICENSE).
