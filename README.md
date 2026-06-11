# Django-Web

A personal portfolio web application built with Python and Django, showcasing skills, experience, and background as a Data Scientist.

## Tech Stack

- Python 3.11
- Django 4.2
- Bootstrap 5
- SQLite3
- HTML / CSS

## Project Structure

```
Django-Web/
├── first_website_project/
│   ├── first_website_project/
│   │   ├── settings.py        # Project settings (uses environment variables)
│   │   ├── urls.py            # Root URL configuration
│   │   ├── wsgi.py            # WSGI entry point
│   │   └── asgi.py            # ASGI entry point
│   ├── homepage/
│   │   ├── templates/
│   │   │   └── homepage/
│   │   │       └── home.html  # Main portfolio page template
│   │   ├── views.py           # View functions
│   │   ├── urls.py            # App URL patterns
│   │   ├── models.py
│   │   └── admin.py
│   ├── staticfiles/
│   │   ├── css/
│   │   │   └── main.css       # Custom stylesheet
│   │   └── images/            # Profile and other images
│   └── manage.py
├── .env.example               # Example environment variables
├── requirements.txt
├── LICENSE
└── README.md
```

## Setup / Installation

### Prerequisites

- Python 3.9 or higher
- pip

### Steps

1. Clone the repository:

```bash
git clone https://github.com/dinnocenzo/Django-Web.git
cd Django-Web
```

2. Create and activate a virtual environment:

```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS / Linux
source venv/bin/activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Set up environment variables by copying the example file:

```bash
cp .env.example .env
```

Edit `.env` and set a secure `SECRET_KEY` for production use.

5. Apply database migrations:

```bash
cd first_website_project
python manage.py migrate
```

6. Collect static files (optional for development):

```bash
python manage.py collectstatic
```

## Usage

Run the development server:

```bash
cd first_website_project
python manage.py runserver
```

Then open your browser and navigate to [http://127.0.0.1:8000/](http://127.0.0.1:8000/) to view the portfolio page.

### Environment Variables

| Variable        | Default                    | Description                          |
|-----------------|----------------------------|--------------------------------------|
| `SECRET_KEY`    | `change-me-in-production`  | Django secret key (set in production)|
| `DEBUG`         | `True`                     | Debug mode toggle                    |
| `ALLOWED_HOSTS` | `localhost,127.0.0.1`      | Comma-separated list of allowed hosts|

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
