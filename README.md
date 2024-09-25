# DaltonSparks.com Django Project

This is a Django-based web application that includes a customizable clock feature. The project is containerized using Docker for easy deployment and development.

## Features

- Responsive design with a dark mode toggle
- Customizable clock with timezone selection
- Draggable and resizable clock interface

## Prerequisites

- Docker
- Docker Compose

## Setup and Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/daltonsparks-django.git
   cd daltonsparks-django
   ```

2. Create a `.env` file in the project root with the following content:
   ```bash
   DJANGO_SECRET_KEY=your_secret_key_here
   DJANGO_DEBUG=True
   DJANGO_ALLOWED_HOSTS=localhost,127.0.0.1
   DB_NAME=django_db
   DB_USER=user
   DB_PASSWORD=password
   DB_HOST=db
   DB_PORT=5432
   ```
   Replace `your_secret_key_here` with a secure random string.

3. Build and run the Docker containers:
   ```bash
   docker-compose up --build
   ```

4. Access the application at `http://localhost:8080`

## Development

- The Django development server will automatically reload when changes are made to the code.
- Static files are served from the `mysite/static` directory.
- Templates are located in the `mysite/templates` directory.

## Deployment

For production deployment:

1. Set `DJANGO_DEBUG=False` in the `.env` file.
2. Update `DJANGO_ALLOWED_HOSTS` with your domain name.
3. Use a production-grade web server like Gunicorn instead of the Django development server.
4. Set up a reverse proxy (e.g., Nginx) to handle static files and SSL termination.
