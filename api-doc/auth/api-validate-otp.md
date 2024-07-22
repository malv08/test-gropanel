[🏠 Back to Home](https://github.com/denitiawan/gropanel-document/blob/main/api-doc/README.md) / [Back To Login Page](https://github.com/denitiawan/gropanel-document/blob/main/api-doc/login/login-page.md)
```
Product Name GroMate
```

## 1. API User Verify
## 2. Description
This API is used to perform Check `Authorization` or Check `Permission` for the `Parent Menu`, `Menu Service`, and `Menu Item` accessible by the user. The data in the HTTP response body will be used on the frontend and visualized in the sidebar menu component. The `Authorization token` in the `HTTP request header` is taken from the `HTTP response body` of the Login API.

## 3. Spesification
### 3.1. URL
```
{{HOST}}/auth/v1/mate/session/verify-user
```
### 3.2. Method
```
POST
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
    "request_id": "e6ece258f883ad4ea23508561e3a5cdd",
    "version": "0.0.1",
    "timestamp": "2024-07-11T01:42:59.600528979Z"
  },
  "payload": {
    "first_name": "Super",
    "last_name": "Admin",
    "role": "super_admin",
    "permission": {
      "all": [
        "all"
      ]
    },
    "locale": "en-US",
    "user_id": 1,
    "scope": "read write",
    "menu": [
      {
        "id": 2,
        "name": "Account Manager",
        "en_name": "Account Manager",
        "sequence": 2,
        "icon_name": "",
        "access_level": 9,
        "background": "",
        "menu_code": "accountmanager",
        "service_menu": [
          {
            "id": 1,
            "parent_menu_id": 2,
            "name": "User Control",
            "en_name": "User Control",
            "sequence": 1,
            "icon_name": "",
            "menu_code": "accountmanager.user-control",
            "access_level": 9,
            "background": "",
            "menu_item": [
              {
                "id": 1,
                "service_menu_id": 1,
                "name": "Principal",
                "en_name": "Principal",
                "sequence": 1,
                "icon_name": "",
                "type": "",
                "menu_code": "accountmanager.user-control.principal",
                "access_level": 9,
                "url": ""
              }
            ]
          }
        ]
      }
    ]
  }
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
curl --location '{{HOST}}/auth/v1/mate/session/verify-user' \
--header 'Authorization: {{AUTHORIZATION_TOKEN}}' \
--header 'Content-Type: application/json' \
```
## 6. Model
```
```
