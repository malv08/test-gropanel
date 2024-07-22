[🏠 Back to Home](https://github.com/denitiawan/gropanel-document/blob/main/api-doc/README.md)
```
Product Name GroPanel Mobile
```
# Auth

### List of APIs
  1. [Login](https://github.com/denitiawan/gropanel-document/blob/main/api-doc/auth/api-login.md)
  2. [Confirm New Device](https://github.com/denitiawan/gropanel-document/blob/main/api-doc/auth/api-confirm-new-device.md)
  3. [Validate OTP](https://github.com/denitiawan/gropanel-document/blob/main/api-doc/auth/api-validate-otp.md)
   
```
# Notes
- api login (hanya verifikasi username, dan password), secara background proses kirim otpke nomor hp 
- api confirmNewDevice (verifikasi device Id, sumber login)
- api validate otp (memvalidasi otp yang dikirim oleh login new device, sumber dari confirm new) -> response body (user_token)


api logout -> req body -> sign (responsevalidate otp : field sign) fungsinnya untuk mendiskonek socket, dan token di redis

semua api headernya 
x-device -> mobile
authorization -> dari api validate otp
```
