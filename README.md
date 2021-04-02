### /register

#### POST
##### Summary

register customer

##### Description
passing customer data to register customer

### Parameter

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| username | body | customer usernmae | Yes | string
| email | body | customer email | Yes | string |
| password | body | customer password | Yes | string |

##### Responses
| Code | Description | 
| ---- | ----------- |
| 200 | success register customer |
| 500 | error registration customer | 

### Body Parameter Example
```json
{
    "username":"lisa233",
    "email":"lisa@gmail5.com",
    "password":"312457"
}
```

## Response Body Example
```json
{    
    "code": 200,
    "message": "success register customers",
    "status": "success"
}
```

### /login

#### POST
##### Summary

login as customer

##### Description
passing email and password to login as customer

###  Parameter
| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| email | body | customer email | Yes | string |
| password | body | customer password | Yes | string |

##### Responses
| Code | Description | 
| ---- | ----------- |
| 200 | success login customer |
| 400 | error login(invalid email/password) | 

### Body Parameter Example
```json
{
   "email":"susi@gmail.com",
   "password":"john123"
}
```

## Response Body Example
```json
{    
    "code": 200,
    "message": "success login customer",
    "status": "success",
    "data": {
        "id": 1,
        "email": "susi@gmail.com",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdXRob3JpemVkIjp0cnVlLCJleHAiOjE2MTczNDg0ODgsInVzZXJJZCI6MX0.C4pvmawkwNP-SVJlIA0qbTct3qen4PPbhtHK9XRRpts"
    }
}
```

