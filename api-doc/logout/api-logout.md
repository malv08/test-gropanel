[🏠 Back to Home](https://github.com/denitiawan/gropanel-document/blob/main/api-doc/README.md) / [Back To Logout Page](https://github.com/denitiawan/gropanel-document/blob/main/api-doc/logout/logout-page.md)
```
Product Name GroMate
```

## 1. API Logout
## 2. Description
This API is used to perform the Logout process. When this process is successful, the `Authorization token will no longer be valid for use`. `To obtain a new Authorization token, the Login API must be executed again`. The `Authorization token in the HTTP request header is taken from the HTTP response body of the Login API`.

## 3. Spesification
### 3.1. URL
```
{{HOST}}/auth/v1/mate/logout
```
### 3.2. Method
```
GET
```
### 3.3. Header
|Key|Value|
|--|--|
|Content-type|application-json|
|Authorization|{{AUTHORIZATION_TOKEN}}|


### 3.4. Request Body (json)
```
```
### 3.5. Request Body (form-data)
```
```
### 3.6. Response Body
```
{
  "success": true,
  "header": {
    "request_id": "09059cde4086a5511fe18203b23a6543",
    "version": "0.0.1",
    "timestamp": "2024-07-14T14:28:48.639213149Z"
  },
  "payload": "Logout successfully"
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
curl --location '{{HOST}}/auth/v1/mate/logout' \
--header 'Authorization: {{AUTHORIZATION_TOKEN}}' \
--header 'Content-Type: application/json' 
```

## 6. Model
```
```
