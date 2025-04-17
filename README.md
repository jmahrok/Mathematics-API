# 🧮 Mathematics API - MuleSoft Implementation

This is a MuleSoft-based API that performs basic arithmetic operations: **Add**, **Subtract**, **Multiply**, and **Divide**. The API accepts two numbers via a JSON body and uses a query parameter to determine the operation.

---

## 📌 API Details

- **Endpoint:** `/calculation`
- **Method:** `POST`
- **Query Parameter:**  
  - `operation` (required): Accepts one of `Add`, `Subtract`, `Multiply`, `Divide`

### 🔸 Request Body (application/json)

```json
{
  "number1": 5,
  "number2": 10
}
