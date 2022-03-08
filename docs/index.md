# Create Account 

Create an Account if  Account does not already exist.

**URL** : `/api/users/signUp`

**Method** : `POST`

**Auth required** : `YES`

**Header** : `Authorization:{jwt-token}`

| Param       |Require |Type     | Description     | 
| :------------- |  :-----------|  :----------- |----------- |
|  username |Yes|  String    | A User name for referencing the account.|
|  password |Yes|  String    | A Password describing the account.|
|  email |Yes|  String    | A Email describing the account.|
|  Role |Yes|  String    | A Select Account of Creator or Viewer.|
|  setupFullname |Yes|  String    | Setup Full name in Setup Account.|
|  birth |Yes|  String    | Data of birth in Setup account |
|  viewerAge |Yes|  String or Boolearn    | Select of viewers under 18 |
|  IDType |Yes|  String    | ID type in Upload your ID |
|  IDFront |Yes| String    | Upload front of your ID in Upload your ID |
|  IDBack |Yes| String    | Upload back of your ID in Upload your ID |
|  CategoryType |Yes|  String    | Select category |




** Success Response: **

**Code** : `200 success`

* Resonse example 

```json
{
   "msg": "User added successfully!!!",
    "data": {}
    }
```

** Error Responses: **

**Condition** : If user already exists, like this msg.

**Code** : `400 BAD REQUEST`

* Content example 

```json
{
    "msg": "User already exists"
}
```

# Get all Account list 

Get the all registered Account list.

**URL** : `/api/users/getSignUp`

**Method** : `GET`

**Auth required** : `YES`

**Header**  : `Authorization:{jwt-token}`


** Success Response: **

**Code** : `200 success`

* Resonse example 


```json
[
    {
        "subscriberPrice": 0,
        "_id": "61c3ccfbaa10e627e8b603ca",
        "username": "steven",
        "email": "Whitehorse@gmail.com",
        "password": "$2a$10$hFILbj6RbCF/ht2E96whVu1y5I3G88hdZCgS5fhRG5aYTZYjDP0ym",
        "role": "creator",
        "birth": "1910-12-12T01:00:00.000Z",
        "viewerAge": "18",
        "IDType": "passport",
        "IDFront": "1640221947241.png",
        "IDBack": "1640221947243.png",
        "CategoryType": "music",
        "date": "2021-12-23T01:12:27.591Z",
        "__v": 0
    }
]
```

**Condition** : Internal Server Error.

**Code** : `500`

* Resonse example 

```json
{
    "msg": "Internal Server error"
}
```

# Login

Login if  Account already exist.

**URL** : `/api/users/login`

**Method** : `POST`

**Auth required** : `YES`

**Header** : `Authorization:{jwt-token}`

| Param       |Require |Type     | Description     | 
| :------------- |  :-----------|  :----------- |----------- |
|  email |Yes|  String    | A Email for logining the account.|
|  password |Yes|  String    | A Password for logining the account.|

** Success Response: **

**Code** : `200 success`

* Resonse example 

```json
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImlkIjoiNjFjM2NjZmJhYTEwZTYyN2U4YjYwM2NhIn0sImlhdCI6MTY0MDIyNTQ1MSwiZXhwIjoxNjQwNjU3NDUxfQ.igb1iqE5HrZYxlIRUJliOiFGxUbNGC-_JfklVNmAyPU"
}
```

** Error Responses: **

**Condition** : If password is wrong, like this msg

**Code** : `400 BAD REQUEST`

* Content example

```json
{
    "errors": [
        {
            "msg": "Invalid Password"
        }
    ]
}
```

**Condition** : If email is wrong, like this msg

**Code** : `400 BAD REQUEST`

* Content example

```json
{
    "errors": [
        {
            "msg": "Invalid Email"
        }
    ]
}
```