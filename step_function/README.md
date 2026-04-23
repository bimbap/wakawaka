# 📦 Order Input – AWS Step Functions

This document describes the **JSON input format** used to start an **AWS Step Functions** workflow for an **Order Management System**.

The JSON payload is provided when calling **StartExecution** and will be processed by multiple states such as **Lambda**, **Choice**, and other workflow steps.

---

## 🧾 Sample JSON Input

```json
{
  "orderId": 1001,
  "customerId": 123,
  "items": [
    {
      "productName": "Laptop Pro",
      "quantity": 1,
      "price": 999.99
    },
    {
      "productName": "Wireless Headphones",
      "quantity": 2,
      "price": 199.99
    }
  ],
  "totalAmount": 1399.97,
  "timestamp": "2024-01-15T10:30:00Z"
}



// curl -X POST \
//   -H "Content-Type: application/json" \
//   -H "x-api-key: uOdjfeTwup71Ps21ALsTr266aBFBwJmo4TPBOwJo" \
//   -d '{
//     "customer_id": "CUST001",
//     "items": [
//       {"product_id": "PROD001", "quantity": 2},
//       {"product_id": "PROD002", "quantity": 1}
//     ]
//   }' \
//   https://z7czukzrs9.execute-api.us-east-1.amazonaws.com/production/orders