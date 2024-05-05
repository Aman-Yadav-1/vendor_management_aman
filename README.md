# Vendor Management System with Performance Metrics

I've developed a Vendor Management System with Performance Metrics, utilizing Django and Django REST Framework, along with a MySQL database and REST API for streamlined vendor management and performance monitoring. Token-based authentication ensures secure API access. This design is entirely my own, without any copied content.

Thank you!

## Features

* **Vendor Management**: Easily create, update, and delete vendor information.
* **Performance Metrics**: Analyze vendor performance using key metrics.
* **RESTful API**: Seamlessly integrate with other systems using RESTful APIs.
* **Token-based Authentication**: Ensure secure user authentication, especially for RESTful APIs.
* **MySQL Database**: Employ MySQL for robust and scalable data storage.

## Advanced Features 🔥

* **On-Time Delivery Rate**
* **Quality Rating Average**
* **Average Response Time**
* **Fulfillment Rate**
* **Vendor Performance**

## Requirements

- Python 3.11
- Django 5.0
- MySQL
- Django REST framework
- rest_framework.authtoken
- Additional Python packages
- Postman

## Installation

1. Import this project into your IDE.
2. Create a new database in MySQL named 'vendor_details'.

## Database Connection

* Utilize the following data for database connection:

```python
DATABASES = {
    'default': {
            'ENGINE': 'django.db.backends.mysql',
            'NAME':'vendor_details',
            'USER':'root',
            'PASSWORD':'root',
            'HOST':'localhost',
            'PORT':'3306',
    }
}
```

* Then in the terminal:
```
py manage.py makemigrations
py manage.py migrate
py manage.py createsuperuser
```

## How to Run

```
py manage.py runserver
```
Navigate to http://127.0.0.1:8000/admin/ to fill in model data, and access the application at http://127.0.0.1:8000/. After opening the URL, access all data by providing a unique vendor ID in the input.

## API Endpoints

API endpoints are available at http://127.0.0.1:8000/api/:

- `api/vendors/<str:vendor_id>/performance/`
- `api/vendors/`
- `api/vendors/<int:vendor_id>/`
- `api/purchase_orders/`
- `api/purchase_orders/<int:po_id>/`
- `api/purchase_orders/<int:po_id>/acknowledge/`

You can test these APIs in Postman using token-based authentication due to global authentication to CBVs.
