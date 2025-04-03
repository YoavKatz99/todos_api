
# Todos API

A simple RESTful API built with Node.js and MongoDB for managing todos. This API allows users to create, read, update, and delete todos, and it uses MongoDB for persistent storage.

## Features

- Create new todos
- Retrieve a list of all todos
- Update existing todos
- Delete todos
- Persist data with MongoDB

## Tech Stack

- **Node.js**: JavaScript runtime built on Chrome's V8 engine
- **Express**: Fast, unopinionated, minimalist web framework for Node.js
- **MongoDB**: NoSQL database used for storing todos
- **Mongoose**: MongoDB object modeling for Node.js
- **dotenv**: Loads environment variables from a `.env` file

## Getting Started

Follow the instructions below to set up and run the project locally.

### Prerequisites

Ensure you have the following installed on your machine:

- [Node.js](https://nodejs.org/) (v14 or higher)
- [MongoDB](https://www.mongodb.com/try/download/community) or a MongoDB Atlas account

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/YoavKatz99/todos_api.git
   cd todos_api
   ```

2. Install the dependencies:

   ```bash
   npm install
   ```

3. Set up environment variables:

   Create a `.env` file in the root directory and add the following:

   ```
   MONGO_URI=your_mongodb_connection_string
   PORT=3000
   ```

   Replace `your_mongodb_connection_string` with your actual MongoDB connection string.

4. Run the app:

   ```bash
   npm start
   ```

   The API will be available at `http://localhost:3000`.

## API Endpoints

### 1. Get All Todos
`GET /todos`

- **Description**: Retrieves all todos from the database.
- **Response**: A list of todos.

### 2. Get a Single Todo
`GET /todos/:id`

- **Description**: Retrieves a specific todo by its ID.
- **Parameters**: `id` (string) – The unique identifier of the todo.
- **Response**: A single todo object.

### 3. Create a New Todo
`POST /todos`

- **Description**: Creates a new todo.
- **Body**: 
   ```json
   {
     "title": "Todo title",
     "description": "Todo description"
   }
   ```
- **Response**: The newly created todo object.

### 4. Update an Existing Todo
`PUT /todos/:id`

- **Description**: Updates an existing todo by its ID.
- **Parameters**: `id` (string) – The unique identifier of the todo.
- **Body**: 
   ```json
   {
     "title": "Updated title",
     "description": "Updated description"
   }
   ```
- **Response**: The updated todo object.

### 5. Delete a Todo
`DELETE /todos/:id`

- **Description**: Deletes a specific todo by its ID.
- **Parameters**: `id` (string) – The unique identifier of the todo.
- **Response**: A success message.

## Contributing

If you want to contribute to this project, feel free to submit a pull request or open an issue. Contributions are always welcome!

1. Fork the repository
2. Create a new branch (`git checkout -b feature-branch`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature-branch`)
5. Create a new pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
