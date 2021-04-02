### /register

#### POST
##### Summary

register customer

##### Description
passing customer data to register customer

### JSON Body parameter
Field | Data Type | Required | Description
--- | --- | --- | ---
username | string| Yes | customer username
email | string | Yes | customer email 
password | string | Yes| customer password

##### Responses
| Code | Description | 
| ---- | ----------- |
| 200 | success register customer |
| 500 | error registration customer | 

### JSON Body Parameter Example
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
        "username":"lisa233",
        "email":"lisa@gmail5.com",
        "password":"312457"
}
```
