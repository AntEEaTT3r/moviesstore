
# GT Movies Store

GT Movies Store is a full-stack movie e-commerce application built with Django and MySQL. Users can browse and search movies, leave reviews, manage a shopping cart, and place orders through a checkout system.

The project focuses on backend development, relational database design, user authentication, and e-commerce functionality.

## Tech Stack

- **Backend:** Python, Django
- **Database:** MySQL, Django ORM
- **Frontend:** HTML, CSS, Django Templates
- **Authentication:** Django's built-in authentication system

## Features

### Movie Catalog
- Browse available movies and view their details.
- Search the movie catalog by title.
- View movie descriptions, images, and user reviews.

### User Authentication
- Register and log into an account.
- Log out securely.
- Access user-specific features and order history.

### Movie Reviews
- Authenticated users can submit movie reviews.
- Users can edit and delete their own reviews.
- Reviews are associated with their respective movies and users.

### Shopping Cart
- Add movies to a session-based shopping cart.
- Manage item quantities.
- Automatically calculate cart totals.
- Maintain cart contents during the browsing session.

### Checkout and Orders
- Complete a checkout workflow.
- Store orders and purchased items in a relational database.
- View previous orders through the user's account.
- Automatically clear the shopping cart after checkout.

**Note:** Checkout records orders in the database. Real payment processing is not implemented.

## Project Structure

```text
moviesstore/
├── accounts/       # Authentication and order history
├── cart/           # Shopping cart, checkout, and order models
├── home/           # Homepage and informational pages
├── movies/         # Movie catalog, search, and reviews
├── moviesstore/    # Django configuration, templates, and static files
├── media/          # Movie images
└── manage.py       # Django management script
```

## Getting Started

### Prerequisites

- Python 3
- MySQL Server
- Django
- Compatible MySQL driver (such as mysqlclient)
- Pillow

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/AntEEaTT3r/moviesstore.git
cd moviesstore
```

**2. Create a virtual environment**

```bash
python -m venv venv
```

Activate the environment:

Windows:
```bash
venv\Scripts\activate
```

macOS/Linux:
```bash
source venv/bin/activate
```

**3. Install dependencies**

Install Django, Pillow, and a compatible MySQL driver for your Python environment.

The project currently does not include a requirements.txt file.

**4. Configure the database**

Create a MySQL database named `moviesstore`.

Update the database connection in `moviesstore/settings.py` with your local MySQL credentials.

Configure a development `SECRET_KEY` and keep credentials out of version control.

**5. Apply database migrations**

```bash
python manage.py migrate
```

**6. Start the development server**

```bash
python manage.py runserver
```

Open:

http://127.0.0.1:8000/

### Admin Access

Create an administrator account:

```bash
python manage.py createsuperuser
```

Access the Django admin interface at:

http://127.0.0.1:8000/admin/

## Database Design

The application uses relational database models to manage:

- Movies and their associated information
- User accounts and authentication
- Movie reviews
- Customer orders
- Individual order items

Django's ORM manages database interactions and relationships between models.

## Screenshots

Screenshots of the application interface will be added here.

Suggested screenshots:
- Movie catalog
- Movie details and reviews
- Shopping cart
- Checkout and order history

## Development Notes

This project was developed as a software engineering and backend development portfolio project.

The application demonstrates Django application architecture, database relationships, authentication, session management, and e-commerce workflows.

The current configuration is intended for local development and is not production-ready.

## License & Terms

© 2026 Anthony Fuller. All rights reserved.

This repository is published solely for portfolio viewing and code demonstration purposes.

Unauthorized copying, modification, or distribution of this code is strictly prohibited.
