
# Projeto Carros

A Django application for managing cars and users.

## Features

- User registration and login
- Car registration
- Car listing and search
- Car details, editing, and deletion
- Image upload

## Requirements

- Python
- Django
- Virtual environment

## Installation

```powershell
git clone https://github.com/Jklimaitis/Projeto_Carros.git
cd Projeto_Carros
python -m venv venv
.\venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
Copy-Item .env.example .env
python manage.py migrate
python manage.py runserver
```
