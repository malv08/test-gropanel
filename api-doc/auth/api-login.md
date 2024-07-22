[🏠 Back to Home](https://github.com/denitiawan/gropanel-document/blob/main/api-doc/README.md) / [Back To Login Page](https://github.com/denitiawan/gropanel-document/blob/main/api-doc/login/login-page.md)
```
Product Name GroMate
```

# 1. API : Login
## 2. Description

## 3. Spesification
### 3.1. URL
```
{{HOST}}/tara/v5/auth/login
```
### 3.2. Method
```
POST
```
### 3.3. Header
|Key|Value|
|--|--|
|Content-type|application-json|
|X-DEVICE|mobile|
|Cookie|i18next=id|

### 3.4. Request Body (json)
```
{
    "userName": "liliktiga",
    "password": "Lilikgro3@",
    "deviceID": "A_7b7f89a25d77" 
}
```
### 3.5. Request Body (form-data)
```
```
### 3.6. Response Body
```
{
  "code": 200,
  "status": 300022,
  "data": {
    "message": "New Device Detected",
    "userModel": {
      "userID": "647ea203dbb5040025861a68",
      "phone": "+6286612346777",
      "firstLogin": 0,
      "userProfiling": "R",
      "isNewDevice": true
    }
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
curl --location 'https://staging-ngchat.gromart.club/tara/v5/auth/login' \
--header 'X-DEVICE: mobile' \
--header 'Content-Type: application/json' \
--header 'Cookie: i18next=id' \
--data-raw '{
    "userName": "liliktiga",
    "password": "Lilikgro3@",
    "deviceID": "A_7b7f89a25d77" 
}
'
```

## 6. Model (Json)
```
{
  "code": "Integer",
  "status": "Integer",
  "data": "Object"
}
----------------------------------
{
  "message": "String",
  "userModel": {
    "userID": "String",
    "phone": "String",
    "firstLogin": "Integer",
    "userProfiling": "String",
    "isNewDevice": "Boolean"
  }
}
```
## 7. Model (Dto)
```java

public class Response {
    private int code;
    private int status;
    private Object data; // UserModel.java
}
----------------------------------
public static class UserModel {
        private String userID;
        private String phone;
        private int firstLogin;
        private String userProfiling;
        private boolean isNewDevice;
}
```
