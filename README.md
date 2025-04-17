
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
```

### 🔸 Sample Request

```bash
curl -X POST "http://localhost:8081/calculation?operation=Add" \
     -H "Content-Type: application/json" \
     -d '{"number1": 5, "number2": 10}'
```

### 🔸 Sample Response

```json
{
  "result": 15
}
```

> ❗ If a division by zero is attempted, the API will return an error message instead of crashing.

---

## 🧠 Supported Operations

| Operation  | Example Input        | Result |
|------------|----------------------|--------|
| Add        | `5 + 10`             | `15`   |
| Subtract   | `10 - 5`             | `5`    |
| Multiply   | `5 * 10`             | `50`   |
| Divide     | `10 / 2`             | `5`    |

---

## 👨‍💻 Author

Developed by Jasdeep Mahrok
---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
