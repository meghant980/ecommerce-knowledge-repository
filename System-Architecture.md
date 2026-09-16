# System Architecture

## Overview

The e-commerce system follows a layered architecture in which the
frontend, backend services, database, and external services work
together to provide online shopping functionality.

## Main Components

### 1. Customer Interface

The customer interacts with the system through a web or mobile
application.

It provides:

- Product browsing
- Product search
- Shopping cart
- Checkout
- Order tracking
- Account management

### 2. Backend Application

The backend handles the main business logic of the system.

It manages:

- User authentication
- Product management
- Cart management
- Order processing
- Inventory
- Payments
- Returns and refunds

### 3. Database

The database stores important business information such as:

- Customer information
- Seller information
- Product information
- Inventory
- Orders
- Payments
- Delivery information
- Reviews

### 4. Payment Service

The payment service processes online transactions and returns the
payment status to the backend.

### 5. Delivery Service

The delivery service manages shipment and delivery information and
updates the status of orders.

## High-Level Architecture

```text
                    E-COMMERCE SYSTEM

                         Customers
                             |
                             v
                    +----------------+
                    | Web / Mobile   |
                    |   Application  |
                    +----------------+
                             |
                             v
                    +----------------+
                    | Backend / API  |
                    +----------------+
                             |
             +---------------+---------------+
             |               |               |
             v               v               v
       +-----------+   +-----------+   +-----------+
       |   User    |   |  Product  |   |   Order   |
       |  Service  |   |  Service  |   |  Service  |
       +-----------+   +-----------+   +-----------+
             |               |               |
             +---------------+---------------+
                             |
                             v
                    +----------------+
                    |    Database    |
                    +----------------+
                             |
                +------------+------------+
                |                         |
                v                         v
        +---------------+         +---------------+
        | Payment       |         | Delivery      |
        | Service       |         | Service       |
        +---------------+         +---------------+
