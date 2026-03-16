# ⚡ FastAPI Learning Project

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-0.100%2B-009688?logo=fastapi&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

A hands-on FastAPI project exploring core concepts including routing, path parameters, query parameters, enums, and type validation — built while following the official FastAPI tutorial series.

---

## 📁 Project Structure

```
FastAPI/
├── from fastapi import FastAPI.py   # Basic app setup and first route
└── main.py                          # Full demo with enums, path params & coupons
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- pip

### Installation

```bash
# Clone the repository
git clone https://github.com/Musawir456/FastAPI.git
cd FastAPI

# Install dependencies
pip install fastapi uvicorn
```

### Running the Server

```bash
uvicorn main:app --reload
```

The API will be available at: `http://127.0.0.1:8000`

Interactive docs (Swagger UI): `http://127.0.0.1:8000/docs`

---

## 📡 API Endpoints

### Basic Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/hello` | Returns a welcome message |
| `GET` | `/hello/{name}` | Returns a personalized welcome message |

**Example:**
```
GET /hello/Musawir
→ "Welcome Musawir"
```

---

### Food Items by Cuisine

```
GET /get_items/{cuisine}
```

Returns a list of food items for the given cuisine type.

**Available Cuisines:**

| Value | Items |
|-------|-------|
| `indian` | Samosa, Dosa |
| `american` | Hot Dog, Apple Pie |
| `italian` | Ravioli, Pizza |

**Example:**
```
GET /get_items/indian
→ ["Samosa", "Dosa"]
```

> Invalid cuisine values are rejected automatically via FastAPI's Enum validation.

---

### Coupon Codes

```
GET /get_coupon/{code}
```

Returns the discount percentage for a given coupon code (integer).

| Code | Discount |
|------|----------|
| `1` | 10% |
| `2` | 20% |
| `3` | 30% |

**Example:**
```
GET /get_coupon/2
→ { "discount_amount": "20%" }
```

---

## 🧠 Concepts Covered

- ✅ FastAPI app initialization
- ✅ Basic `GET` route creation
- ✅ Path parameters (string and integer)
- ✅ Python `Enum` for constrained input values
- ✅ Type coercion and validation
- ✅ Auto-generated interactive API documentation

---

## 📚 Resources

- [FastAPI Official Documentation](https://fastapi.tiangolo.com/)
- [FastAPI Tutorial – User Guide](https://fastapi.tiangolo.com/tutorial/)
- [Uvicorn ASGI Server](https://www.uvicorn.org/)

---

## 👤 Author

**Musawir456**  
GitHub: [@Musawir456](https://github.com/Musawir456)

---

> 📌 *This project is part of an ongoing FastAPI learning journey. More endpoints and features will be added as the tutorial progresses.*
