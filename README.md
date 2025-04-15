# Task Management API

## 📌 Overview

A lightweight RESTful API built with **Node.js** and **Express** for basic task (to-do) management. The API uses **in-memory storage** and includes **Swagger UI documentation** for easy testing and visualization.

---

## 🚀 Features

- Basic CRUD operations (Create, Read, Update, Delete)
- In-memory data handling (no DB setup required)
- Error handling with status codes
- Swagger documentation at `/api-docs`
- Sample data added on server start

---

## 🔧 Installation & Running

```bash
git clone https://github.com/shreyash0019/Assignment-Backend.git
cd task-api
npm install
node index.js
```

Visit: [http://localhost:3000/api-docs](http://localhost:3000/api-docs) for API UI documentation

---

## 📂 Endpoints

### ✅ `GET /tasks`
- Fetch all tasks

### ✅ `GET /tasks/:id`
- Fetch a specific task by ID

### ✅ `POST /tasks`
- Create a new task
- Request Body:
```json
{
  "title": "Task title",
  "description": "Task description"
}
```

### ✅ `PUT /tasks/:id`
- Update a task by ID
- Request Body:
```json
{
  "title": "Updated title",
  "description": "Updated description"
}
```

### ✅ `DELETE /tasks/:id`
- Delete a task by ID

---

## 📘 API Docs (Swagger)

URL: [http://localhost:3000/api-docs](http://localhost:3000/api-docs)

Auto-generated from inline JSDoc comments using `swagger-jsdoc` and `swagger-ui-express`.

---

## 💡 Sample Tasks on Startup
```json
[
  {
    "id": 1,
    "title": "Design homepage",
    "description": "Create wireframes for the homepage"
  },
  {
    "id": 2,
    "title": "API integration",
    "description": "Connect frontend with backend REST API"
  }
]
```

---

## 📄 Swagger Comments (Example for GET /tasks)

In `index.js`, make sure comments look like this:

```js
/**
 * @swagger
 * /tasks:
 *   get:
 *     summary: Retrieve all tasks
 *     tags: [Tasks]
 *     responses:
 *       200:
 *         description: A list of tasks
 *         content:
 *           application/json:
 *             schema:
 *               type: array
 *               items:
 *                 type: object
 *                 properties:
 *                   id:
 *                     type: integer
 *                   title:
 *                     type: string
 *                   description:
 *                     type: string
 */
```

Add similar blocks for POST, PUT, DELETE endpoints as needed.

---

> For any issues or ideas, feel free to contribute or raise an issue in the repository.

