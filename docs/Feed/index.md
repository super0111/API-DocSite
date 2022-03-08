# View contents

View contents on feed page

**URL** : `/api/posts/`

**Method** : `GET`

**Auth required** : `YES`

**Header** : `Authorization:{jwt-token}`

** Success Response: **

**Code** : `200 success`

* Resonse example 

```json
[
    {
        "comments": [
            {
                "_id": "61c3ea4baa10e627e8b603ee",
                "comments": "music is good for man",
                "date": "2021-12-23T03:17:31.062Z",
                "userId": "61c3ccfbaa10e627e8b603ca",
                "__v": 0
            }
        ],
        "tips": [],
        "likes": [],
        "_id": "61c3e62aaa10e627e8b603e0",
        "userID": "61c3ccfbaa10e627e8b603ca",
        "contentImg": "1640228394550.png",
        "description": "this is design",
        "price": "800",
        "contentType": "design",
        "date": "2021-12-23T02:59:54.553Z",
        "__v": 0
    }
]
```

# Put Comments

Put comments about selected content by viewer on feed page.

**URL** : `/api/posts/:id/comments`
** id : current selected content ID **

**Method** : `POST`

**Auth required** : `YES`

| Param       |Require |Type     | Description     | 
| :------------- |  :-----------|  :----------- |----------- |
|  comments |Yes|  String    | put comments by current viewer.|
|  userId |Yes|  String    | Current Viewer userId.|

**Header** : `Authorization:{jwt-token}`

** Success Response: **

**Code** : `200 success`

* Resonse example 

```json
{
    "comments": [
        "61c3ea4baa10e627e8b603ee"
    ],
    "tips": [],
    "likes": [],
    "_id": "61c3e62aaa10e627e8b603e0",
    "userID": "61c3ccfbaa10e627e8b603ca",
    "contentImg": "1640228394550.png",
    "description": "this is design",
    "price": "800",
    "contentType": "design",
    "date": "2021-12-23T02:59:54.553Z",
    "__v": 0
}
```

# Give Tip

Give tip about selected content by current viewer

**URL** : `/api/posts/:id/giveTip`
** id : ID of one content **

**Method** : `POST`

**Auth required** : `YES`

| Param       |Require |Type     | Description     | 
| :------------- |  :-----------|  :----------- |----------- |
|  tipPrice |Yes|  Number    | Give tip by current viewer.|
|  tipMessage |Yes|  String    | Give message by current viewer.|
|  userId |Yes|  String    | Current Viewer userId.|

**Header**  : `Authorization:{jwt-token}`


** Success Response: **

**Code** : `200 success`

* Resonse example 


```json
{
    "comments": [
        "61c3ea4baa10e627e8b603ee"
    ],
    "tips": [
        "61c3ebe9aa10e627e8b603f3"
    ],
    "likes": [],
    "_id": "61c3e62aaa10e627e8b603e0",
    "userID": "61c3ccfbaa10e627e8b603ca",
    "contentImg": "1640228394550.png",
    "description": "this is design",
    "price": "800",
    "contentType": "design",
    "date": "2021-12-23T02:59:54.553Z",
    "__v": 0
}
```

# Give Like

Give like follow about selected content by current viewer

**URL** : `/api/posts/:id/likes`
** id : ID of one content **

**Method** : `POST`

**Auth required** : `YES`

| Param       |Require |Type     | Description     | 
| :------------- |  :-----------|  :----------- |----------- |
|  userId |Yes|  String    | Current Viewer userId.|

**Header**  : `Authorization:{jwt-token}`


** Success Response: **

**Code** : `200 success`

* Resonse example 

```json
{
    "comments": [
        "61c3ea4baa10e627e8b603ee"
    ],
    "tips": [
        "61c3ebe9aa10e627e8b603f3",
        "61c3ebf1aa10e627e8b603f6"
    ],
    "likes": [
        "61c3ec7caa10e627e8b603fa"
    ],
    "_id": "61c3e62aaa10e627e8b603e0",
    "userID": "61c3ccfbaa10e627e8b603ca",
    "contentImg": "1640228394550.png",
    "description": "this is design",
    "price": "800",
    "contentType": "design",
    "date": "2021-12-23T02:59:54.553Z",
    "__v": 0
}
```
** Error Responses: **

**Condition** : If view already puted like follow, like this msg

**Code** : `400 BAD REQUEST`

* Content example

```json
{
    "Like": "already have done"
}
```

**Condition** : Internal Server Error.

**Code** : `500`

* Resonse example 

```json
{
    "msg": "Internal Server error"
}
```