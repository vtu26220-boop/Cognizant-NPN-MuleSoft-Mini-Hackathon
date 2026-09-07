# Order Management API

## Project Overview

This project is a MuleSoft-based Order Management API developed as a mini-hackathon project.

The API accepts customer order details, validates the request, checks product availability and stock, calculates the order subtotal, applies a 10% discount for orders above ₹10,000, creates the order, and sends a notification.

## Architecture

Postman / Client
        |
        v
Order Management API
        |
        v
Request Validation
        |
        v
Product API
        |
        v
Stock Check
        |
        v
Subtotal & Discount Calculation
        |
        v
Order Management API
        |
        v
Notification API
        |
        v
Final Response

## Main API

### Create Order

**Method:** POST

**Endpoint:**

`http://localhost:8081/orders`

### Request Example

```json
{
  "customerId": "CUST001",
  "customerName": "Pradeep",
  "customerEmail": "pradeep@gmail.com",
  "items": [
    {
      "productId": "P001",
      "quantity": 2
    },
    {
      "productId": "P002",
      "quantity": 1
    }
  ]
}