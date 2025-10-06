# 🧩 Task Manager API

A simple yet powerful **Task Management API** built with **FastAPI** and **SQLModel**.  
This project allows you to **create, read, update, and delete tasks** through RESTful APIs and includes a lightweight **web-based UI** for quick task management.

---

## 🚀 Features

- 🗂️ Create, Read, Update, and Delete (CRUD) tasks  
- 🔍 Filter tasks by status, priority, or search query  
- 🕒 Track due dates and creation timestamps  
- ✅ Mark tasks as complete or pending  
- 💻 Interactive built-in HTML UI  
- 🧠 Backed by **SQLite** for simplicity and portability  
- ⚡ Built with **FastAPI** for high performance  

---

## 🧠 Tech Stack

- **Python 3.9+**
- **FastAPI** — Web Framework  
- **SQLModel** — ORM (by Tiangolo, combines Pydantic & SQLAlchemy)  
- **SQLite** — Database (default)  
- **Uvicorn** — ASGI server for development  

---

## 📦 Installation

Follow the steps below to run the project locally.


### 1. Clone the Repository
```bash
git clone https://github.com/your-username/task-manager-api.git
cd task-manager-api
```

```bash
python3 -m venv venv
source venv/bin/activate
```

```bash
pip install -r requirements.txt
```

---

## 🧱 Project Structure

| File / Folder         | Description                       |
|----------------------|-----------------------------------|
| `main.py`            | Main FastAPI application          |
| `tasks.db`           | SQLite database file              |
| `requirements.txt`   | Python dependencies               |
| `README.md`          | Project documentation             |


---

## 🧭 API Endpoints

| **Method** | **Endpoint**         | **Description**              |
|-------------|----------------------|------------------------------|
| `GET`       | `/`                  | Web UI for managing tasks    |
| `GET`       | `/tasks/`            | List all tasks               |
| `GET`       | `/tasks/{task_id}`   | Get a specific task          |
| `POST`      | `/tasks/`            | Create a new task            |
| `PATCH`     | `/tasks/{task_id}`   | Update an existing task      |
| `DELETE`    | `/tasks/{task_id}`   | Delete a task                |
| `GET`       | `/health`            | Health check endpoint        |

---

## 🧩 Example Request (Create Task)

**POST** `/tasks/`

**Request Body:**
```json
{
  "title": "Prepare project presentation",
  "description": "Create slides and rehearse for the upcoming demo",
  "priority": 1,
  "due_date": "2025-10-12"
}
```

**Response:**

```json
{
  "id": 5,
  "title": "Prepare project presentation",
  "description": "Create slides and rehearse for the upcoming demo",
  "done": false,
  "priority": 1,
  "due_date": "2025-10-12",
  "created_at": "2025-10-06T15:45:22Z"
}
```

---

## 🧑‍💻 Usage (Web UI)

1. Open your browser
2. Add tasks using the input fields  
3. Mark tasks as **done** or edit them inline  
4. Tasks are automatically persisted to the **SQLite** database  

---

## 🧑‍🤝‍🧑 Contributors

**Prince Patel**

---

## 🛡️ License

This project is licensed under the **MIT License**.  
You are free to use, modify, and distribute this project with proper attribution.
