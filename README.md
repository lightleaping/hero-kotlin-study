# 📚 Hero Tech Kotlin 학습 저장소

본 저장소는 Hero Tech Course 2026 준비를 위한  
Kotlin 학습 및 Spring Boot 실습 기록 공간입니다.

---

## 🔗 목차

1. [01_kotlin_basic](./01_kotlin_basic) - Kotlin 문법 입문
2. [02_spring_mvc](./02_spring_mvc) - Spring Boot MVC 실습
3. [03_book_app](./03_book_app) - 도서관리 실전 프로젝트

---

# 📘 Kotlin Spring Boot REST API Practice

This repository contains step-by-step REST API practice built using **Kotlin + Spring Boot**. Each API endpoint demonstrates a key concept in request handling such as `@GetMapping`, `@RequestParam`, `@PathVariable`, and object binding.

## ✅ Features Implemented

### 1️⃣ Basic String Response

GET /api/hello  
**Response:**  
hello kotlin

---

### 2️⃣ Path Variable Mapping

GET /api/get-mapping/path-variable/{name}/{age}  
**Example:** /api/get-mapping/path-variable/Soojin/24  
**Response:** Soojin 24

GET /api/get-mapping/path-variable2/{name}/{age}  
Demonstrates Kotlin variable shadowing vs URL value extraction

---

### 3️⃣ Query Parameter Mapping

GET /api/get-mapping/query-param?name=Soojin&age=24  
**Response:** Soojin 24

---

### 4️⃣ Object Mapping (DTO)

GET /api/get-mapping/query-param/object?name=Soojin&age=24&email=test@example.com&address=Seoul  
Maps all query parameters into a `UserRequest` data class  
**Response (JSON):**

{
  "name": "Soojin",
  "age": 24,
  "email": "test@example.com",
  "address": "Seoul"
}

---

### 5️⃣ Query Parameters as Map

GET /api/get-mapping/query-param/map?name=Alex&age=30&phone-number=1234  
Handles query parameters dynamically as a Map<String, Any>

---

## 🧾 Data Class

```kotlin
data class UserRequest (
    var name: String? = null,
    var age: Int? = null,
    var email: String? = null,
    var address: String? = null
)
```
🛠 How to Run
Make sure you have JDK 17+ and Gradle installed.
---
./gradlew bootRun
---
Then open:
http://localhost:8080/api/hello
Use Talend API Tester or Postman for parameterized requests.

📁 Project Structure
src
└── main
  └── kotlin
    └── com.example.mvc
      ├── MvcApplication.kt
      ├── controller.get.GetApiController.kt
      └── model.http.UserRequest.kt

✍️ Author
Created and maintained by Soojin
Feel free to fork or contribute!

📝 License
This project is licensed under the MIT License.
