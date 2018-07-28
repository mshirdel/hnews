# hnews

This repository represents APIs for a sample web site like hackernews. My main idea was about learning Ruby on Rails for back-end and React for front-end so I design an API to implement for both back-end and fornt-end.

## Implementations
[Rails Ripository](https://github.com/mshirdel/rails_hnews)

## List of APIs

Name    | URI               | Verb
-----   | --------------    | ------------------
Registration | api/users | POST
Login | api/users/login | POST
Get Current User | api/user | GET

---

## APIs Descriptions

### Registration (Sign Up new user)

```
POST api/users
```
#### body
```json
{
  "user":
  {
    "email":"email@example.com", 
    "password":"pasword", 
    "username":"example"
  }
}
```
#### Result
```json
{
  "user": {
      "id": 5,
      "email": "email@example.com",
      "username": "example",
      "bio": null,
      "token": "eyJhbGciOiJIUzI1NiJ9.eyJpZCI6NSwiZXhwIjoxNTM3OTQ0ODM2fQ.OAenR46hZ4Yk0a2fpvlqMd9819BZGjKuWVQcv01iTew"
  }
}
```
### Login

```
POST api/users/login
```

#### body
```json
{
  "user": {
    "email":"email@example.com",
    "password":"pasword"
    }
}
```

#### Result
```json
{
  "user": {
      "id": 5,
      "email": "email@example.com",
      "username": "example",
      "bio": null,
      "token": "eyJhbGciOiJIUzI1NiJ9.eyJpZCI6NCwiZXhwIjoxNTM3ODk2NTE0fQ.FqTup-cjeec-Jd8g9u8oLTICG8ksq-nzBoS8SPNDcDo"
  }
}
```

### Current User
```
GET /api/user
```

#### header
```
  Authorization: Token {{token}}
```

#### Result
```json
{
  "user": {
      "id": 5,
      "email": "email@example.com",
      "username": "example",
      "bio": null,
      "token": "eyJhbGciOiJIUzI1NiJ9.eyJpZCI6NCwiZXhwIjoxNTM3OTQ1Mjk0fQ.zm88z-EjicCxoD8vcEAwGmb6kQWd0gBgztLtdxZfd3A"
  }
}
```
