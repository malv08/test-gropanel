[🏠 Back to Home](https://github.com/denitiawan/gropanel-document/blob/main/api-doc/README.md)
```
Product Name GroMate
```

# 1. Overview
## 1.1. Description
This document contains information about the APIs in the GroMate project. The purpose of this document is as an `API Contract` and `as one part of the Technical Document` for this GroMate project.

## 1.2. Generate Postman Collection
These documents can be uploaded to `Chat AI` such as `Chat GPT`. And later it can be degenerated into a postman collection file. With the example command below :
<img src="https://github.com/user-attachments/assets/05f24a64-6a1b-4f8e-afc4-c945207bf79b" alt="image" width="600">
```
Base on file  i was uploaded, can you convert into postman collection files
```

## 1.3. Generate Token & Akses APIs
All APIs in the GroMate project have an `Authorization` Token which must be filled in in the `http request header` section. Below is the sequence diagram for getting tokens.
<img src="https://github.com/user-attachments/assets/74182af6-63ec-45c1-8feb-ea87581d24c1" alt="image" width="600" >

## 1.4. Server
Below is the server information for GroMate.

### 1.4.1. Staging
```
Name : GroMate
Version : 1.0.0
Url : https://staging-core.grocloud.id
ENV : {{HOST}}
```

### 1.4.2. Sandbox
```
Name : GroMate
Version : 1.0.0
Url : https://sandbox-mate.grocloud.id
ENV : {{HOST}}
```
### 1.4.3. Production
```
Name : GroMate
Version : 1.0.0
Url : https://mate.grocloud.id
ENV : {{HOST}}
```
