[🏠 Back to Home](https://github.com/denitiawan/gropanel-document/blob/main/api-doc/README.md) / [Back To Login Page](https://github.com/denitiawan/gropanel-document/blob/main/api-doc/login/login-page.md)
```
Product Name GroMate
```

# 1. API Login
<img src="https://github.com/user-attachments/assets/96d88944-216c-4f36-b9d0-ec9f4d0aaae2" alt="image" width="500">

## 2. Description
API for performing authentication using a `username` and `password`. If the authentication process is successful, it will generate an `Authorization` token in the `HTTP request body`, which can be used to `access all APIs on GroMate`. 

## 3. Spesification
### 3.1. URL
```
{{HOST}}/auth/v1/mate/login
```
### 3.2. Method
```
POST
```
### 3.3. Header
|Key|Value|
|--|--|
|Content-type|application-json|

### 3.4. Request Body (json)
```
{
  "username": "nexSoft",
  "password": "nexSoft1!"
}
```
### 3.5. Request Body (form-data)
```
```
### 3.6. Response Body
```
{
  "success": true,
  "header": {
    "request_id": "12302f38d2125f6c508e68ddaf47da1f",
    "version": "0.0.1",
    "timestamp": "2024-07-11T01:42:59.528800563Z"
  },
  "payload": "xxxx.xxxx.xxxx"
}
```
### 3.7. Response Header
```
```

## 4. Message
|Http Status|Message|
|--|--|
|200|Success|

## 5. CURL
```
curl --location '{{HOST}}/auth/v1/mate/login' \
--header 'Authorization: {{AUTHORIZATION_TOKEN}}' \
--header 'Content-Type: application/json' \
--data '{
  "username": "nexSoft",
  "password": "nexSoft1!"
}'
```

## 6. Model
```
{
  "username": "String",
  "password": "String"
}
```
