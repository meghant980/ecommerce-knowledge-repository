# APIs

## Overview

APIs (Application Programming Interfaces) allow different components
of the e-commerce system to communicate with each other.

The backend can provide REST APIs for users, products, carts, orders,
payments, and deliveries.

## User APIs

### Register User

**Method:** POST

**Endpoint:**
`/api/users/register`

Creates a new customer or seller account.

### Login

**Method:** POST

**Endpoint:**
`/api/users/login`

Authenticates a registered user.

### Get User Profile

**Method:** GET

**Endpoint:**
`/api/users/profile`

Returns information about the logged-in user.

## Product APIs

### Get Products

**Method:** GET

**Endpoint:**
`/api/products`

Returns a list of available products.

### Get Product Details

**Method:** GET

**Endpoint:**
`/api/products/{product_id}`

Returns detailed information about a specific product.

### Add Product

**Method:** POST

**Endpoint:**
`/api/products`

Allows an authorized seller to add a product.

### Update Product

**Method:** PUT

**Endpoint:**
`/api/products/{product_id}`

Updates product information.

### Delete Product

**Method:** DELETE

**Endpoint:**
`/api/products/{product_id}`

Removes a product from the platform.

## Cart APIs

### Add to Cart

**Method:** POST

**Endpoint:**
`/api/cart`

Adds a product to the customer's cart.

### View Cart

**Method:** GET

**Endpoint:**
`/api/cart`

Returns the customer's current cart.

### Remove from Cart

**Method:** DELETE

**Endpoint:**
`/api/cart/{product_id}`

Removes a product from the cart.

## Order APIs

### Create Order

**Method:** POST

**Endpoint:**
`/api/orders`

Creates a new order after checkout.

### Get Orders

**Method:** GET

**Endpoint:**
`/api/orders`

Returns the customer's orders.

### Get Order Details

**Method:** GET

**Endpoint:**
`/api/orders/{order_id}`

Returns details of a specific order.

### Cancel Order

**Method:** PUT

**Endpoint:**
`/api/orders/{order_id}/cancel`

Cancels an eligible order.

## Payment API

### Process Payment

**Method:** POST

**Endpoint:**
`/api/payments`

Processes payment for an order.

### Payment Status

**Method:** GET

**Endpoint:**
`/api/payments/{payment_id}`

Returns the status of a payment transaction.

## Delivery APIs

### Track Order

**Method:** GET

**Endpoint:**
`/api/delivery/{order_id}`

Returns the current delivery status of an order.

### Update Delivery Status

**Method:** PUT

**Endpoint:**
`/api/delivery/{order_id}`

Allows authorized delivery personnel to update delivery status.

## API Security

APIs should use:

- Authentication
- Authorization
- HTTPS
- Input validation
- Rate limiting
- Secure error handling
- Access control

## Conclusion

APIs provide a standardized way for the frontend, backend, database,
payment services, and delivery services to communicate within the
e-commerce system.
