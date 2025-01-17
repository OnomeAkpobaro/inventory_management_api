Inventory Management API

A robust REST API built with Django and Django Rest Framework for managing inventory items across multiple stores. This API provides comprehensive inventory management capabilities including item tracking, user authentication, and detailed reporting.

Features
Core Functionality

1. Complete Inventory Management

Create, read, update, and delete inventory items
Track item details including name, description, quantity, price, and category
Monitor inventory levels across different locations
Historical tracking of inventory changes


2. Account Management

Secure user authentication and authorization
Role-based access control
Individual user inventory management


3. Advanced Inventory Tracking

Real-time inventory level monitoring
Category-based organization
Low stock alerts
Detailed change history logging



4. Technical Features

RESTful API design using Django Rest Framework
Secure authentication system
Efficient pagination and sorting
Comprehensive error handling
Database optimization with Django ORM


Authentication:

POST /api/accounts/login/
POST /api/accounts/register/

Inventory Management
GET    /api/inventory/            # List all items
POST   /api/inventory/            # Create new item
GET    /api/inventory/{id}/       # Get specific item
PUT    /api/inventory/{id}/       # Update item
DELETE /api/inventory/{id}/       # Delete item


End Points:

http://nomzzy.pythonanywhere.com/api/inventory/categories/
http://nomzzy.pythonanywhere.com/api/inventory/categories/<pk>/
http://nomzzy.pythonanywhere.com/api/inventory/inventory-items/
http://nomzzy.pythonanywhere.com/api/inventory/inventory-items/<pk>/
http://nomzzy.pythonanywhere.com/api/inventory/inventory-items/<pk>/adjust_stock/
http://nomzzy.pythonanywhere.com/api/inventory/inventory-changes/
http://nomzzy.pythonanywhere.com/api/inventory/inventory-changes/<pk>/
http://nomzzy.pythonanywhere.com/api/inventory/supplier/
http://nomzzy.pythonanywhere.com/api/inventory/supplier/<pk>/
http://nomzzy.pythonanywhere.com/api/inventory/stores/
http://nomzzy.pythonanywhere.com/api/inventory/stores/<pk>/
http://nomzzy.pythonanywhere.com/api/inventory/store-inventory/
http://nomzzy.pythonanywhere.com/api/inventory/store-inventory/<pk>/
http://nomzzy.pythonanywhere.com/api/inventory/alerts/
http://nomzzy.pythonanywhere.com/api/inventory/alerts/<pk>/
http://nomzzy.pythonanywhere.com/api/inventory/alerts/<pk>/resolve_alert/



POSTMAN TEST:
CATEGORY

GET :
http://nomzzy.pythonanywhere.com/api/inventory/categories/

POST:
http://nomzzy.pythonanywhere.com/api/inventory/categories/
input: 
{
    "name": " ",
    "description": " ",
}

PUT:
http://nomzzy.pythonanywhere.com/api/inventory/categories/

DELETE:
http://nomzzy.pythonanywhere.com/api/inventory/categories/


SUPPLIER

GET:
http://nomzzy.pythonanywhere.com/api/inventory/suppliers/

POST:
http://nomzzy.pythonanywhere.com/api/inventory/suppliers/
input:
{
    "name": " ",
    "contact_person": "",
    "email": "",
    "phone" = "",
    "address" = "",
}
PUT:
http://nomzzy.pythonanywhere.com/api/inventory/suppliers/

DELETE:
http://nomzzy.pythonanywhere.com/api/inventory/suppliers/


Stock-report:

GET:
http://nomzzy.pythonanywhere.com/api/inventory/reports/stock/

Inventory Alerts:
GET
http://nomzzy.pythonanywhere.com/api/inventory/alerts/<pk>/

Resolve alert:
POST:
http://nomzzy.pythonanywhere.com/api/inventory/alerts/<pk>/resolve_alert/




STORE

GET:
http://nomzzy.pythonanywhere.com/api/inventory/stores/

POST:
http://nomzzy.pythonanywhere.com/api/inventory/stores/
input:
{
    "name": " ",
    "address" = "",
    "contact_number": "",
    "email": ""
    
    
}
PUT:
http://nomzzy.pythonanywhere.com/api/inventory/stores/

DELETE:
http://nomzzy.pythonanywhere.com/api/inventory/stores/



STORE-INVENTORY
GET
http://nomzzy.pythonanywhere.com/api/inventory/store-inventory/

POST
http://nomzzy.pythonanywhere.com/api/inventory/store-inventory/
{
    "store": "1",
    "item": "5",
    "quantity": 400
}

