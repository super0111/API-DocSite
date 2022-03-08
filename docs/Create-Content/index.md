# Create Content

Create an content by creator.

**URL** : `/api/posts`

**Method** : `POST`

**Auth required** : `YES`

**Header** : `Authorization:{jwt-token}`

| Param       |Require |Type     | Description     | 
| :------------- |  :-----------|  :----------- |----------- |
|  description |Yes|  String    | A Description for content.|
|  price |Yes|  Number    | A Price for showing content.|
|  contentImg |Yes|  String    | A Content Image for content.|
|  userID |Yes|  String    | A user ID for current creator.|
|  contentType |Yes|  String    | content type.|

** Success Response: **

**Code** : `200 success`

* Resonse example 

```json
{
    "comments": [],
    "tips": [],
    "likes": [],
    "_id": "61c3ddf4aa10e627e8b603d1",
    "userID": "61c362c6f6fca119a498b1d1",
    "contentImg": "1640226292352.png",
    "description": "this is design",
    "price": "800",
    "contentType": "design",
    "date": "2021-12-23T02:24:52.355Z",
    "__v": 0
}
```

# Get Contents 

Get the all posted contents.

**URL** : `/api/posts`

**Method** : `GET`

**Auth required** : `YES`

**Header**  : `Authorization:{jwt-token}`


** Success Response: **

**Code** : `200 success`

* Resonse example 


```json
[
    {
        "comments": [
            {
                "_id": "61c3612ef6fca119a498b1c9",
                "comments": "music is good for man",
                "date": "2021-12-22T17:32:30.438Z",
                "userId": "61c36108f6fca119a498b1c3",
                "__v": 0
            }
        ],
        "tips": [],
        "likes": [],
        "_id": "61c36119f6fca119a498b1c6",
        "userID": "61c36108f6fca119a498b1c3",
        "contentImg": "1640194329373.png",
        "description": "this is picture",
        "price": "800",
        "contentType": "picture",
        "date": "2021-12-22T17:32:09.376Z",
        "__v": 0
    },
    {
        "comments": [],
        "tips": [],
        "likes": [],
        "_id": "61c3ddf4aa10e627e8b603d1",
        "userID": "61c362c6f6fca119a498b1d1",
        "contentImg": "1640226292352.png",
        "description": "this is design",
        "price": "800",
        "contentType": "design",
        "date": "2021-12-23T02:24:52.355Z",
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