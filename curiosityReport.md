# Curiosity Report: JSON Web Tokens
## What is it?
JSON web token (JWT) is a standard used across the web for providing a trustworthy signature when communicating information. This provides a verifiable and reliable way to ensure that users are authorized and information is coming from a trusted source.
## Structure
A JWT is made of three pieces, which are then encoded and separated by dots.
### Header
The first segment is the header, which denotes the type of token (JWT) and the algorithm used to sign it, such as RSA.
```json
{
  "alg": "RSA",
  "typ": "JWT"
}
```
### Payload
The second portion contains the claims about the user, such as their admin status and the time the token was issued. There are some registered claims defined by the JWT specification, but custom claims can be used as well.
```json
{
    "name": "Kate",
    "admin": "true"
}
```
### Signature
To verify the message is not corrupted, the header and payload are encoded and concatented, then run through the algorithm specified in the header using a shared secret.  
  
Each of the three parts are encoded with base 64 URL encoding and separated by dots.

## How are they used?
When a user log in to an application using JWTs, a JWT is returned, which can then be stored in an Authorization header for future HTTP requests to prove the user's identity.

## Benefits
JWTs are a helpful tool for authentiction and communication because they:
- Are relatively small in length (compared to other tokens)
- Use JSON, which is easy to parse
- Easy to sign and encode
- Commonly used across the Internet
- Signature and issuer can be verified with ease