# Library Management System - Setup & Usage Guide

<img width="4000" height="3000" alt="collage (1)" src="https://github.com/user-attachments/assets/62d17e0f-0935-4689-9426-871b0768d080" />



## Installation

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Run migrations:
```bash
python manage.py migrate
```

3. Start the server:
```bash
python manage.py runserver
```

4. Access the app:
- **Browser UI**: http://localhost:8000/
- **Admin Panel**: http://localhost:8000/admin/
- **API Endpoints**: http://localhost:8000/api/books/

## Admin Credentials

- **Username**: admin
- **Password**: AdminPass123

## API Endpoints

### GET /api/books/
Retrieve all books

### POST /api/books/
Create a new book
```json
{
  "title": "Django for Beginners",
  "author_name": "John Doe",
  "author_email": "john@example.com",
  "isbn": "9780123456789",
  "published_date": "2023-01-15",
  "is_available": true
}
```

### GET /api/books/<id>/
Get a specific book

### PUT /api/books/<id>/
Update a book

### DELETE /api/books/<id>/
Delete a book

## Features

✅ REST API for all HTTP methods (GET, POST, PUT, DELETE)
✅ Django admin interface for book and author management
✅ Professional browser UI with full CRUD functionality
✅ Internal CSS and JavaScript for seamless UX
✅ Author auto-create on book submission
✅ SQLite database with proper relationships

## Project Structure

```
library_project/
├── books/
│   ├── migrations/
│   ├── templates/books/
│   │   └── book_admin.html
│   ├── models.py (Author, Book)
│   ├── views.py (REST API views)
│   ├── serializers.py (DRF serializers)
│   ├── urls.py (URL routing)
│   ├── admin.py (Admin registration)
│   └── tests.py
├── library_project/
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── manage.py
├── db.sqlite3
└── requirements.txt
```
