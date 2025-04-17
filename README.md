
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

## 📂 Project Structure

```
mathematics-api/
├── src/
│   └── main/
│       └── mule/
│           └── math-operation-flow.xml
├── README.md
├── .gitignore
```

---

## 🧰 Technologies Used

- MuleSoft Anypoint Studio 7.x
- Mule Runtime 4.x
- DataWeave 2.0
- HTTP Listener

---

## 🚀 How to Run Locally

1. Import the project into **Anypoint Studio**
2. Run the Mule application
3. Test with Postman, curl, or browser (for GET requests if added)

---

## ☁️ How to Push This Project to GitHub (Mac Terminal)

```bash
# Navigate to your project folder
cd /path/to/mathematics-api

# Initialize a git repo
git init

# Add your GitHub repo as remote
git remote add origin https://github.com/YOUR_USERNAME/mathematics-api.git

# Stage and commit your files
git add .
git commit -m "Initial commit - MuleSoft Mathematics API"

# Set default branch to main and push
git branch -M main
git push -u origin main
```

---

## 🧾 .gitignore (Recommended)

Create a `.gitignore` file and add:

```
# MuleSoft / Anypoint Studio specific
target/
.project
.classpath
.settings/
.idea/
*.iml
.DS_Store
```

---

## 👨‍💻 Author

Developed by [Your Name]  
📧 your.email@example.com  
🌐 [LinkedIn / Portfolio](https://www.linkedin.com/)

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
