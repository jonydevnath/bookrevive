# BookRevive

BookRevive is a Django-based online bookstore and e-commerce project for selling old books and managing customer orders. The application includes product browsing, a shopping cart, checkout, user profile management, and an admin dashboard for product and order administration.

## Features

- Product catalog with category browsing
- Search for books by name or description
- User registration and login flow
- Customer profile and shipping information updates
- Shopping cart with persisted session support
- Checkout with shipping details and payment method options
- Order placement and order history
- Admin dashboard for product and order management
- Product upload and editing support
- Responsive storefront styling with Bootstrap

## Tech Stack

- Python
- Django 4.2
- SQLite (default) / PostgreSQL-compatible configuration
- Bootstrap for frontend styling
- Pillow for image handling
- django-environ for environment configuration
- Whitenoise for static file serving

## Project Structure

- `store/` – storefront, product listings, search, login, registration, and profile logic
- `cart/` – shopping cart implementation and session-based cart management
- `payment/` – checkout, order processing, shipping data, and admin payment dashboard
- `ecom/` – Django project settings and URL routing
- `static/` – CSS, JavaScript, and frontend assets
- `media/` – uploaded product images and local media files

## Prerequisites

- Python 3.10+
- pip
- virtualenv or venv

## Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd bookrevive
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file in the project root with the required environment variables:

   ```env
   ENVIRONMENT=development
   SECRET_KEY=your-secret-key-here
   DATABASE_URL=sqlite:////absolute/path/to/your/project/db.sqlite3
   ```

   If you are using PostgreSQL instead of SQLite, use a PostgreSQL connection string such as:

   ```env
   DATABASE_URL=postgres://username:password@localhost:5432/bookrevive
   ```

5. Run database migrations:

   ```bash
   python manage.py migrate
   ```

6. Create an admin account:

   ```bash
   python manage.py createsuperuser
   ```

## Running the Application

Start the Django development server:

```bash
python manage.py runserver
```

Then open the app in your browser:

```text
http://127.0.0.1:8000/
```

To access the admin panel:

```text
http://127.0.0.1:8000/admin/
```

## Production Notes

This project is configured with WhiteNoise and a production-ready deployment setup for Vercel. For production deployments, update the environment variables and ensure `SECRET_KEY` and `DATABASE_URL` are set correctly.

To collect static files for production:

```bash
python manage.py collectstatic
```

## Common Commands

- Start server:

  ```bash
  python manage.py runserver
  ```

- Create migrations:

  ```bash
  python manage.py makemigrations
  ```

- Apply migrations:

  ```bash
  python manage.py migrate
  ```

- Open Django shell:

  ```bash
  python manage.py shell
  ```

## License

This project is provided as a learning/demo e-commerce project. Update the licensing terms as needed for your own deployment.
