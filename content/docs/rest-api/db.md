---
weight: 2
title: "Database content"
---


## **General Overview**
**Moxly RestAPI** provides an interface for managing users, system settings, and database content via HTTP requests. All requests require authentication using a Bearer Token.

---

## 🔑 **Authentication**
- **Type:** Bearer Token  
- **Header:** `Authorization: Bearer <SECRET_TOKEN>`  

---


### 📌 **3.1 Get Database Contents**
- **Method:** `GET`  
- **URL:** `https://<YOUR_SITE>/rest-api/database`  
- **Query Parameters:**  
   - `limit`: Number of records (default: 10)  
   - `page`: Page number (default: 1)  
   - `sort_field`: Field to sort by  
   - `sort_order`: Sort direction  
   - `secret`: Database secret key (required)  
- **Response:** JSON array of records  

---

### 📌 **3.2 Get Database Content Item by ID**
- **Method:** `GET`  
- **URL:** `https://<YOUR_SITE>/rest-api/database/{id}`  
- **Parameters:**  
   - `secret`: Database secret key  
- **Response:** Data of the specific item  

---

### 📌 **3.3 Update Database Content Item**
- **Method:** `PUT`  
- **URL:** `https://<YOUR_SITE>/rest-api/database/{id}`  
- **Request Body (JSON):**  
```json
{
    "Name": "test testov",
    "Recipe_History": "bla bla bla",
    "categories": [124995, 124997]
}
```
- **Query Parameters:**  
   - `secret`: Database secret key  
- **Response:** Update status  

---

### 📌 **3.4 Add Database Content Item**
- **Method:** `POST`  
- **URL:** `https://<YOUR_SITE>/rest-api/database`  
- **Request Body (JSON):**  
```json
{
    "Name": "test testov",
    "categories": [124995, 124997],
    "Recipe_History": "bla bla bla"
}
```
- **Query Parameters:**  
   - `secret`: Database secret key  
- **Response:** New item data  

---

### 📌 **3.5 Delete Database Content Item**
- **Method:** `DELETE`  
- **URL:** `https://<YOUR_SITE>/rest-api/database/{id}`  
- **Query Parameters:**  
   - `secret`: Database secret key  
- **Response:** Deletion status  

---

## 📊 **Response Status Codes**
- **200 OK:** Successful request  
- **400 Bad Request:** Invalid request  
- **401 Unauthorized:** Missing or invalid token  
- **403 Forbidden:** Access denied  
- **404 Not Found:** Resource not found  
- **500 Internal Server Error:** Server-side error  

---

## 📝 **Notes**
- `Authorization: Bearer <SECRET_TOKEN>` must be included in all requests.  
- Some operations require the `secret` parameter for additional security.  

---

**For additional support, contact the API administrator.**
