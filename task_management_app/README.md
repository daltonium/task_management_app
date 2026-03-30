# 📋 Task Management App

A full-stack task management web application built with **Django** and **PostgreSQL**, containerized with **Docker**.

---

## 🚀 Features

- ✅ User registration & login / logout
- ✅ Create, view, edit, and delete tasks
- ✅ Task status — Pending / Completed
- ✅ Priority levels — High / Medium / Low
- ✅ Due dates
- ✅ User-isolated tasks (each user sees only their own)
- ✅ Responsive gradient UI

---

## 🛠️ Tech Stack

| Layer      | Technology          |
|------------|---------------------|
| Backend    | Django 6.x (Python) |
| Database   | PostgreSQL 16       |
| Frontend   | HTML, CSS (custom)  |
| Container  | Docker + Compose    |

---

## 📁 Project Structure
task_management_app/
├── manage.py
├── Dockerfile
├── docker-compose.yml
├── .env
├── .dockerignore
├── requirements.txt
├── static/
│ └── css/
│ └── style.css
├── task_management_app/
│ ├── settings.py
│ ├── urls.py
│ └── wsgi.py
└── tasks/
├── models.py
├── views.py
├── forms.py
├── urls.py
├── admin.py
└── templates/
└── tasks/
├── base.html
├── login.html
├── register.html
├── task_list.html
├── task_form.html
├── task_detail.html
└── task_confirm_delete.html

text

---

## ⚙️ Setup & Run (with Docker)

### Prerequisites
- [Docker Desktop](https://www.docker.com/products/docker-desktop/) installed and running

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/task_management_app.git
cd task_management_app
```

### 2. Create the `.env` file
```bash
cp .env.example .env
```
Edit `.env` and set your own `SECRET_KEY` and `DB_PASSWORD`.

### 3. Build and start containers
```bash
docker compose up --build
```

### 4. Create a superuser (in a new terminal)
```bash
docker compose exec web python manage.py createsuperuser
```

### 5. Open the app
http://127.0.0.1:8000/

text

### 6. Stop the containers
```bash
docker compose down
```

---

## ⚙️ Setup & Run (without Docker)

### 1. Create and activate virtual environment
```bash
python -m venv venv
venv\Scripts\activate       # Windows
source venv/bin/activate    # macOS/Linux
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Configure PostgreSQL
Update `settings.py` with your local database credentials.

### 4. Run migrations
```bash
python manage.py migrate
```

### 5. Create superuser
```bash
python manage.py createsuperuser
```

### 6. Start server
```bash
python manage.py runserver
```

---

## 🐳 Useful Docker Commands

```bash
docker compose up --build       # Build and start all containers
docker compose up -d            # Start in background (detached mode)
docker compose down             # Stop all containers
docker compose logs web         # View Django logs
docker compose logs db          # View PostgreSQL logs
docker compose exec web bash    # Open shell inside Django container
docker compose exec web python manage.py migrate
docker compose exec web python manage.py createsuperuser
```

---

## 🔐 Environment Variables

| Variable      | Description                  | Default           |
|---------------|------------------------------|-------------------|
| `DEBUG`       | Django debug mode (1 or 0)   | `1`               |
| `SECRET_KEY`  | Django secret key            | change this!      |
| `DB_NAME`     | PostgreSQL database name     | `task_manager_db` |
| `DB_USER`     | PostgreSQL username          | `task_manager_user` |
| `DB_PASSWORD` | PostgreSQL password          | `yourpassword`    |
| `DB_HOST`     | Database host                | `db`              |
| `DB_PORT`     | Database port                | `5432`            |

---

## 📚 What I Learned

- Django MVT architecture (Models, Views, Templates)
- Django ORM and database migrations
- User authentication with `django.contrib.auth`
- ModelForms and form validation
- PostgreSQL integration with `psycopg2`
- Docker containerization and Docker Compose
- Static files configuration
- Environment variable management

---

## 📄 License

This project is for learning purposes.
Final Folder Structure
text
task_management_app/        ← project root
├── Dockerfile
├── docker-compose.yml
├── .env                    ← never commit this
├── .dockerignore
├── requirements.txt
├── README.md
├── manage.py
├── static/
├── task_management_app/
└── tasks/

