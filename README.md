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

### Request Body Parameter Example
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

### Request Body Parameter Example
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
### /customers

### /customers/{id}

#### PUT
##### Summary

Update Customer Data

##### Description
passing several data to update  customer data 

###  Parameter
| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | customer id | Yes | string |
| email | body | customer email | No | string |
| adresss | body | customer address | No | string |
| bank_name | body | customer email | No | string |
| bank_account_number | body | customer address | No | string |

##### Responses
| Code | Description | 
| ---- | ----------- |
| 200 | success update customer data |
| 400 | error update data| 

### Request Body Parameter Example
```json
{
    "email":"32ibu@gmail.com",
    "address": "jalan ahmad yani",
    "bank_name": "BCA",
    "bank_account_number": "23232323"
}
```

## Response Body Example
```json
{    
    "code": 200,
    "message": "success update profil customer",
    "status": "success"
}
```

### /products

### /products?category={id}

#### GET
##### Summary

Get products

##### Description
Get all product based on category, if no id is passed then it will return all product in the store

###  Parameter
| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | query | category id | No | int |

##### Responses
| Code | Description | 
| ---- | ----------- |
| 200 | success get products |
| 400 | error bad request | 


## Response Body Example
```json
{    
    "code": 200,
    "message": "success get product",
    "status": "success",
    "data":  [
        {
            "id": 1,
            "name": "Yonex Zerox",
            "categories_id": 4,
            "description": "Raket tercepat di Asia",
            "quantity": 30,
            "price": 45000,
            "unit": "pcs",
            "CreatedAt": "2021-03-28T20:01:40.21+07:00",
            "UpdatedAt": "2021-03-28T20:01:40.21+07:00"
        }
    ]
}
```

### /cartitems

#### POST
##### Summary

Adding cartitems to carts

##### Description
Adding product that customer wants to buy into their cart

###  Parameter
| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| carts_id | body | customer cart id | Yes | int |
| products_id | body | product id | Yes | int |
| quanitty | body | quantity of product | Yes | int |

##### Responses
| Code | Description | 
| ---- | ----------- |
| 200 | success insert cartitems |
| 400 | invalid input| 
| 500 | product/cart not exist|

### Request Body Parameter Example
```json
{
    "carts_id":4,
    "products_id":9,
    "quantity":3
}
```

## Response Body Example
```json
{    
    "code": 200,
    "status": "success",
    "message": "success insert cartitems"
}
```
