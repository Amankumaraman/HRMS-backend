# HRMS Lite – Backend (Django REST API)

## Overview

HRMS Lite Backend is a lightweight Human Resource Management System API built using **Django REST Framework**.
It provides RESTful APIs to manage employees and track daily attendance.

This project was developed as part of a Full-Stack Coding Assignment focusing on clean architecture, API design, validation, and deployment readiness.

---

## Live API

Base URL:

https://hrms-backend-f5nw.onrender.com/api/

Example Endpoint:

GET /employees/

---

## Features

* Employee Management

  * Add employee
  * View employee list
  * Delete employee
* Attendance Management

  * Mark attendance (Present / Absent)
  * View attendance records
* Server-side validation
* Duplicate prevention
* Proper HTTP status codes
* Error handling
* Production deployment using Gunicorn

---

## Tech Stack

* Python
* Django 5
* Django REST Framework
* SQLite (for simplicity)
* Gunicorn
* WhiteNoise
* Render (Deployment)

---

## API Endpoints

### Employees

| Method | Endpoint             | Description     |
| ------ | -------------------- | --------------- |
| GET    | /api/employees/      | List employees  |
| POST   | /api/employees/      | Add employee    |
| DELETE | /api/employees/{id}/ | Delete employee |

### Attendance

| Method | Endpoint         | Description     |
| ------ | ---------------- | --------------- |
| GET    | /api/attendance/ | View attendance |
| POST   | /api/attendance/ | Mark attendance |

---

## Data Validation

* Unique Employee ID
* Valid email format
* Required fields validation
* Prevent duplicate attendance per day

---

## Run Locally

### 1. Clone repository

git clone <repo-url>

cd hrms

### 2. Create virtual environment

python -m venv venv

venv\Scripts\activate

### 3. Install dependencies

pip install -r requirements.txt

### 4. Run migrations

python manage.py migrate

### 5. Start server

python manage.py runserver

Server runs at:

http://127.0.0.1:8000/

---

## Deployment

Backend deployed on **Render** using:

* Gunicorn WSGI server
* WhiteNoise static handling
* Public API access

---

## Assumptions

* Single admin user
* Authentication not required (as per assignment scope)
* Minimal HR features only

---

## Future Improvements

* Authentication & roles
* PostgreSQL database
* Dashboard analytics
* Pagination & filtering
* Docker containerization

---

## Author

Aman Kumar
Python Backend Developer
