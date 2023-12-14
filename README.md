# Social Media API README

## Overview

This project is a social media API designed to support a social networking website. The API utilizes a NoSQL database, specifically MongoDB, to efficiently handle large amounts of unstructured data. The key functionalities include handling users, thoughts, and reactions.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Acceptance Criteria](#acceptance-criteria)
- [API Routes](#api-routes)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Installation

To set up the social media API, follow these steps:

1. Clone the repository to your local machine.
   ```bash
   git clone https://github.com/your-username/social-media-api.git
   ```

2. Navigate to the project directory.
   ```bash
   cd social-media-api
   ```

3. Install the dependencies.
   ```bash
   npm install
   ```

## Usage

1. Ensure that you have MongoDB installed and running on your machine.

2. Create a `.env` file in the root directory and configure the following variables:

   ```env
   MONGODB_URI=your_mongodb_connection_string
   ```

3. Start the server.
   ```bash
   npm start
   ```

## Acceptance Criteria

### Server Initialization

- When you enter the command to invoke the application, the server is started, and the Mongoose models are synced to the MongoDB database.

### User and Thought Routes

- When you open API GET routes in Insomnia for users and thoughts, the data for each of these routes is displayed in a formatted JSON.

### CRUD Operations

- When you test API POST, PUT, and DELETE routes in Insomnia, you should be able to successfully create, update, and delete users and thoughts in the database.

### Reactions

- When you test API POST and DELETE routes in Insomnia for reactions, you should be able to successfully create and delete reactions.

## API Routes

- **GET /api/users**: Get all users.
- **GET /api/users/:userId**: Get a specific user by ID.
- **POST /api/users**: Create a new user.
- **PUT /api/users/:userId**: Update a user by ID.
- **DELETE /api/users/:userId**: Delete a user by ID.

- **GET /api/thoughts**: Get all thoughts.
- **GET /api/thoughts/:thoughtId**: Get a specific thought by ID.
- **POST /api/thoughts**: Create a new thought.
- **PUT /api/thoughts/:thoughtId**: Update a thought by ID.
- **DELETE /api/thoughts/:thoughtId**: Delete a thought by ID.

- **POST /api/reactions/:thoughtId**: Add a reaction to a thought.
- **DELETE /api/reactions/:thoughtId/:reactionId**: Remove a reaction from a thought.

## Examples

### Get Users

```bash
curl http://localhost:3001/api/users
```

## License

This project is licensed under the [MIT License](LICENSE).