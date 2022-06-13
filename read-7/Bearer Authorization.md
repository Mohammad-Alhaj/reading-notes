## JWT
---
JSON Web Token (JWT) it used to securely transfer the information between tow bodes or tow server 

and *open standard (RFC 7519)* 


### *When should you use JSON Web Tokens?*

---

- *Authorization :* allowing the user to access routes, services, and resources that are permitted with that token. 

- *Information Exchange :* JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed

### *What is the JSON Web Token structure?*

 - Header

 - Payload

 - signture

 **JWT typically looks like the following...**

 `xxxxxxx.yyyyyyy.zzzzzzz`

 ---

 #### **Header**

 The header typically consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as` HMAC SHA256 or RSA.`

**JSON is Base64Url encoded to form the first part of the JWT**
 ```
 {
  "alg": "HS256",
  "typ": "JWT"
}
```
---
### **Payload**

There are three types of claims : 

- Registered claims: There are predefined  claims it's not mandatory but recommended 
Some of them are: iss (issuer), exp (expiration time), sub (subject), aud (audience), and others.

- Public claims : these can be defined at will by those using JWTs. But to avoid collisions they should be defined in the IANA JSON Web Token Registry or be defined as a URI that contains a collision resistant namespace.

- Private claims : These are the custom claims created to share information between parties that agree on using them and are neither registered or public claims.

```
{
  "sub": "1234567890",
  "name": "John Doe",
  "admin": true
}

```
---

payload or header elements of a JWT unless it is encrypted.

### **Signature**

To create the signature part you have to take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that.

For example if you want to use the HMAC SHA256 algorithm, the signature will be created in the following way:


```

HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  secret)
  ```
