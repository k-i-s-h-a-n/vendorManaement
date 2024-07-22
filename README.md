# Vendor Management System with Performance Metrics

## Overview

This project is a Vendor Management System built using Django and Django REST Framework. It handles vendor profiles, tracks purchase orders, and calculates vendor performance metrics.

## Features

1. **Vendor Profile Management:**
   - CRUD operations for vendor profiles.
   - Store vendor information including name, contact details, address, and a unique vendor code.

2. **Purchase Order Tracking:**
   - CRUD operations for purchase orders.
   - Track fields like PO number, vendor reference, order date, items, quantity, and status.

3. **Vendor Performance Evaluation:**
   - Calculate metrics: on-time delivery rate, quality rating, response time, and fulfilment rate.
   - Store performance metrics in the vendor model and historical performance data.

## Installation

### Prerequisites

- Python 
- Django 
- Django REST Framework
- Sqlite,PostgreSQL,SQL (or any preferred database)

### Steps

1. Clone the repository:   
   - git clone <repository_url>
   - cd <repository_directory>

2. Create a virtual environment:
    - python -m venv venv
    - source venv/bin/activate  # On Windows use `venv\Scripts\activate`

3. Install the required packages:
    - pip install -r requirements.txt

4. Apply migrations:
    - python manage.py makemigrations
    - python manage.py migrate

5. Create a superuser:
   - python manage.py createsuperuser

6.Run the development server:
  - python manage.py runserver


##API Endpoints
1.Vendor Management
  - POST /api/vendors/: Create a new vendor.
  - GET /api/vendors/: List all vendors.
  - GET /api/vendors/{vendor_id}/: Retrieve vendor details.
  - PUT /api/vendors/{vendor_id}/: Update vendor details.
  - DELETE /api/vendors/{vendor_id}/: Delete a vendor.
  
2.Purchase Order Tracking
  - POST /api/purchase_orders/: Create a purchase order.
  - GET /api/purchase_orders/: List all purchase orders.
  - GET /api/purchase_orders/{po_id}/: Retrieve purchase order details.
  - PUT /api/purchase_orders/{po_id}/: Update a purchase order.
  - DELETE /api/purchase_orders/{po_id}/: Delete a purchase order.
  
3.Vendor Performance Evaluation
  - GET /api/vendors/{vendor_id}/performance: Retrieve vendor performance metrics.


