 Database Design

Overview

The e-commerce system requires a database to store and manage
information related to users, products, orders, payments, inventory,
and deliveries.

Main Entities

 1. User

Stores information about customers, sellers, and administrators.

Main attributes:

- User ID
- Name
- Email
- Phone Number
- Password
- Role
- Address

2. Product

Stores information about products available on the platform.

Main attributes:

- Product ID
- Product Name
- Description
- Category
- Price
- Seller ID
- Stock Quantity
- Rating

3. Cart

Stores products selected by a customer before checkout.

Main attributes:

- Cart ID
- User ID
- Product ID
- Quantity
- Total Amount

4. Order

Stores information about customer orders.

Main attributes:

- Order ID
- Customer ID
- Order Date
- Total Amount
- Order Status
- Delivery Address
5. Order Item

Stores individual products included in an order.

Main attributes:

- Order Item ID
- Order ID
- Product ID
- Quantity
- Product Price

6. Payment

Stores information about transactions.

Main attributes:

- Payment ID
- Order ID
- Payment Method
- Transaction ID
- Amount
- Payment Status
- Payment Date

7. Inventory

Stores product stock information.

Main attributes:

- Inventory ID
- Product ID
- Available Quantity
- Last Updated

8. Delivery

Stores shipment and delivery information.

Main attributes:

- Delivery ID
- Order ID
- Delivery Partner ID
- Shipping Address
- Delivery Status
- Estimated Delivery Date

 9. Review

Stores customer feedback about products.

Main attributes:

- Review ID
- Product ID
- Customer ID
- Rating
- Review Text
- Review Date

Entity Relationships

The main relationships are:

- One customer can place multiple orders.
- One order can contain multiple order items.
- One product can appear in multiple order items.
- One seller can manage multiple products.
- One product has inventory information.
- One order can have a payment transaction.
- One order can have delivery information.
- A customer can write multiple product reviews.

 Simplified Database Structure

```text
User
 |
 +----< Order
 |        |
 |        +----< Order Item >---- Product
 |                                |
 |                                +---- Inventory
 |                                |
 |                                +----< Review
 |
 +----< Review

Order
 |
 +---- Payment
 |
 +---- Delivery

Seller
 |
 +----< Product
