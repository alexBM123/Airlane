# Airline Reservation System (Django)

A full-stack Django web application that models an airline reservation system, supporting flights, airports, passengers, and authenticated users. Built as part of **Harvard CS50’s Web Programming with Python and JavaScript**, this project demonstrates relational data modeling, Django ORM usage, authentication, and clean separation of concerns in a production-style web app.

---

## Motivation

Airline systems are a classic example of relational data problems: flights connect airports, passengers book multiple flights, and users interact with the system securely.  
This project was built to deeply understand:

- Relational database design (one-to-many, many-to-many)
- Django’s ORM and migration system
- Server-side rendering with templates
- Authentication and authorization using Django’s built-in tools

The goal was to build a **clean, extensible, database-driven web application** rather than a toy demo.

---

## Features

- **Flight Management**
  - View all flights
  - View detailed flight pages
  - Associate origin and destination airports
- **Airport Modeling**
  - Airports stored as first-class entities (city + IATA code)
  - Reverse relations for arrivals and departures
- **Passenger Management**
  - Many-to-many relationship between passengers and flights
  - Add passengers to flights via web UI
  - Prevent duplicate passenger bookings
- **Admin Interface**
  - Fully functional Django Admin for managing airports, flights, and passengers
  - Customized admin views for improved usability
- **User Authentication**
  - Login / logout functionality
  - Auth-protected pages
  - Session-based authentication using Django’s auth system
- **Clean Architecture**
  - Modular Django apps (`flights`, `users`)
  - ORM-driven database interactions (no raw SQL)

---

## Tech Stack

### Backend
- Python 3
- Django

### Frontend
- Django Templates (HTML)
- Server-side rendering

### Database
- SQLite (default Django configuration)
- Django Migrations

---

## High-Level Architecture

```
airline/
├── airline/
├── flights/
├── users/
├── db.sqlite3
└── manage.py
```

---

## Setup & Installation

```bash
git clone https://github.com/your-username/airline-django.git
cd airline-django
python -m venv venv
source venv/bin/activate
pip install django
```

---

## Database Setup

```bash
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
```

---

## Running the Project

```bash
python manage.py runserver
```

---

## Future Improvements

- REST API (Django REST Framework)
- PostgreSQL for production
- Search and filtering
- Pagination
- Frontend framework integration
