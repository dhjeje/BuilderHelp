---
weight: 3
title: "System data"
---


## **General Overview**
**Moxly RestAPI** provides an interface for managing users, system settings, and database content via HTTP requests. All requests require authentication using a Bearer Token.

---

## 🔑 **Authentication**
- **Type:** Bearer Token  
- **Header:** `Authorization: Bearer <SECRET_TOKEN>`  

---


## ⚙️ **1. System data**

### 📌 **1.1 Check Connection**
- **Method:** `GET`  
- **URL:** `http://127.0.0.1:8000/rest-api/test`  
- **Response:** Server status  

---

### 📌 **1.2 Get Application Data**
- **Method:** `GET`  
- **URL:** `https://<YOUR_SITE>/rest-api/application`  
- **Response:** Application information  

---

## 📝 **Notes**
- `Authorization: Bearer <SECRET_TOKEN>` must be included in all requests.  
- Some operations require the `secret` parameter for additional security.  

---

**For additional support, contact the API administrator.**