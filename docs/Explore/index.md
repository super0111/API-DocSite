# Content View

View content by user on explore page.

**URL** : `/api/explore/getByUser`

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
        "comments": [
            {
                "_id": "61c36324f6fca119a498b1db",
                "comments": "music is good for man",
                "date": "2021-12-22T17:40:52.938Z",
                "userId": "61c362c6f6fca119a498b1d1",
                "__v": 0
            }
        ],
        "tips": [],
        "likes": [],
        "_id": "61c362ebf6fca119a498b1d4",
        "userID": "61c362c6f6fca119a498b1d1",
        "contentImg": "1640194795547.png",
        "description": "this is design",
        "price": "800",
        "contentType": "design",
        "date": "2021-12-22T17:39:55.549Z",
        "__v": 0
    },
]
```

# More details 

View content details of a creator.

**URL** : `/api/explore/:id/moredetail`
** id : ID of one content **

**Method** : `GET`

**Auth required** : `YES`

**Header**  : `Authorization:{jwt-token}`


** Success Response: **

**Code** : `200 success`

* Resonse example 


```json
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