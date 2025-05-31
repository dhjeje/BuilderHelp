---
weight: 4
title: "Users"
---


## **General Overview**
**Moxly RestAPI** provides an interface for managing users, system settings, and database content via HTTP requests. All requests require authentication using a Bearer Token.

---

## 🔑 **Authentication**
- **Type:** Bearer Token  
- **Header:** `Authorization: Bearer <SECRET_TOKEN>`  

---

## 👤 **1. Users**

### 📌 **1.1 Get a List of Users**
- **Method:** `GET`  
- **URL:** `https://<YOUR_SITE>/rest-api/users`  
- **Query Parameters:**  
   - `limit` (int): Number of records (default: 10)  
   - `page` (int): Page number (default: 1)  
   - `sort_field` (string): Field to sort by (optional)  
   - `sort_order` (string): Sort direction (`asc`/`desc`, optional)  
- **Response:** JSON array of users  

---

### 📌 **1.2 Get User by ID**
- **Method:** `GET`  
- **URL:** `http://<YOUR_SITE>/rest-api/users/{id}`  
- **Parameters:**  
   - `{id}`: User ID  
- **Response:** User data  

---

### 📌 **1.3 Update User by ID**
- **Method:** `PUT`  
- **URL:** `https://<YOUR_SITE>/rest-api/users/{id}`  
- **Request Body (JSON):**  
```json
{
    "name": "Name21",
    "lastname": "Last Name21",
    "custom_fields": {
        "ddduser_name": "Username test123"
    }
}
```
- **Response:** Update status  

---

### 📌 **1.4 Add New User**
- **Method:** `POST`  
- **URL:** `https://<YOUR_SITE>/rest-api/users`  
- **Request Body (JSON):**  
```json
{
    "name": "Name2",
    "lastname": "Last Name2",
    "custom_fields": {
        "ddduser_name": "Username test123"
    }
}
```
- **Response:** New user data  

---

### 📌 **1.5 Delete User by ID**
- **Method:** `DELETE`  
- **URL:** `https://<YOUR_SITE>/rest-api/users/{id}`  
- **Response:** Deletion status  

---

## 📝 **Notes**
- `Authorization: Bearer <SECRET_TOKEN>` must be included in all requests.  
- Some operations require the `secret` parameter for additional security.  

---

**For additional support, contact the API administrator.**