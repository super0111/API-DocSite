# View profile

view profile of current logined user on profile secton of Setting page

**URL** : `/api/profile/getUser/:id`
** id : current logined user ID **

**Method** : `GET`

**Auth required** : `YES`

**Header** : `Authorization:{jwt-token}`

** Success Response: **

**Code** : `200 success`

* Resonse example 

```json
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
```

# Get comments

Get comments about logined user on profile section.

**URL** : `/api/profile/comments/:id`
** id : current logined user id **

**Method** : `GET`

**Auth required** : `YES`

**Header** : `Authorization:{jwt-token}`

** Success Response: **

**Code** : `200 success`

* Resonse example 

```json
{
    "message": "success",
    "data": [
        {
            "_id": "61c3e9ecaa10e627e8b603e9",
            "comments": "music is good for man",
            "date": "2021-12-23T03:15:56.372Z",
            "userId": "61c3e60faa10e627e8b603da",
            "__v": 0
        },
        {
            "_id": "61c3ea4baa10e627e8b603ee",
            "comments": "music is good for man",
            "date": "2021-12-23T03:17:31.062Z",
            "userId": "61c3ccfbaa10e627e8b603ca",
            "__v": 0
        }
    ]
}
```

# Edit Profile

Edit profile of current logined User on profile section.

**URL** : `/api/profile/:id/edit`
** id : current logined User Id **

**Method** : `PUT`

**Auth required** : `YES`

| Param       |Require |Type     | Description     | 
| :------------- |  :-----------|  :----------- |----------- |
|  username |Yes|  String    | Username of current User.|
|  email |Yes|  String    | Email of current User.|
|  IDFront |Yes|  String    | IDFront of current User.|

**Header**  : `Authorization:{jwt-token}`


** Success Response: **

**Code** : `200 success`

* Resonse example 


```json
{
    "edit": {
        "subscriberPrice": 0,
        "_id": "61c3ccfbaa10e627e8b603ca",
        "email": "kungfu@gmail.com",
        "password": "$2a$10$hFILbj6RbCF/ht2E96whVu1y5I3G88hdZCgS5fhRG5aYTZYjDP0ym",
        "role": "creator",
        "birth": "1910-12-12T01:00:00.000Z",
        "viewerAge": "18",
        "IDType": "passport",
        "IDFront": "1640231433440.png",
        "IDBack": "1640221947243.png",
        "CategoryType": "music",
        "date": "2021-12-23T01:12:27.591Z",
        "__v": 0
    }
}
```

# Add following

Add following creator.

**URL** : `/api/profile/:id/following`
** id : current logined viewer Id **

**Method** : `POST`

**Auth required** : `YES`

| Param       |Require |Type     | Description     | 
| :------------- |  :-----------|  :----------- |----------- |
|  creatorId |Yes|  String    | Creator Id of following creator.|

**Header**  : `Authorization:{jwt-token}`


** Success Response: **

**Code** : `200 success`

* Resonse example 


```json
{
    "_id": "61c409f900ee9c2964b8c80b",
    "viewId": "61c406e500ee9c2964b8c7fc",
    "creatorId": "61c409e300ee9c2964b8c808",
    "status": true,
    "__v": 0
}
```

# Get following user

Get following creator.

**URL** : `/api/profile/:id/following`
** id : current logined viewer Id **

**Method** : `GET`

**Auth required** : `YES`

**Header**  : `Authorization:{jwt-token}`


** Success Response: **

**Code** : `200 success`

* Resonse example 

```json
{
    "message": "success",
    "data": [
        {
            "subscriberPrice": 0,
            "_id": "61c409e300ee9c2964b8c808",
            "username": "Sven",
            "email": "Sven@gmail.com",
            "password": "$2a$10$kwts5IMJFxabm/NldhL4puoWdCtYptkSx.5.dG.XiCQy1T8Xwu4u.",
            "role": "creator",
            "birth": "1910-12-12T01:00:00.000Z",
            "viewerAge": "18",
            "IDType": "passport",
            "IDFront": "1640237538218.png",
            "IDBack": "1640237538218.png",
            "CategoryType": "music",
            "date": "2021-12-23T05:32:19.007Z",
            "__v": 0
        }
    ]
}
```


# Pay subscribe

Pay subscriber price by viewer

**URL** : `/api/profile/:id/paySubscribe`
** id : current logined viewer Id **

**Method** : `POST`

**Auth required** : `YES`

| Param       |Require |Type     | Description     | 
| :------------- |  :-----------|  :----------- |----------- |
|  subscribePrice |Yes|  Number    | SubscribePrice of following creator.|
|  creatorId |Yes|  String    | Creator Id of following creator.|

**Header**  : `Authorization:{jwt-token}`


** Success Response: **

**Code** : `200 success`

* Resonse example 


```json
{
    "tips": [],
    "coinAmounts": [],
    "_id": "61c40cf500ee9c2964b8c80f",
    "creatorId": "61c3675d94cc5027e8089525",
    "viewId": "61c406e500ee9c2964b8c7fc",
    "subscribePrice": 200,
    "date": "2021-12-23T05:45:25.531Z",
    "__v": 0
}
```

# Get Subscriber

Get subscriber of current logined User on Subscriber section.

**URL** : `/api/profile/:id/subscriber`
** id : current logined User Id **

**Method** : `GET`

**Auth required** : `YES`

**Header**  : `Authorization:{jwt-token}`


** Success Response: **

**Code** : `200 success`

* Resonse example 


```json
{
    "subscriberPrice": 0,
    "_id": "61c406e500ee9c2964b8c7fc",
    "username": "steven",
    "email": "Whitehorse@gmail.com",
    "password": "$2a$10$zsgwPUzldThHrsTvARJ0Uurb7d4rHu4BaWf4CCw.8rQm0KkJll2Za",
    "role": "viewer",
    "birth": "1910-12-12T01:00:00.000Z",
    "viewerAge": "18",
    "IDType": "passport",
    "IDFront": "1640236772969.png",
    "IDBack": "1640236772971.png",
    "CategoryType": "music",
    "date": "2021-12-23T05:19:33.250Z",
    "__v": 0
}
```

# Put Subscriber

Put subscriber of current logined User on Subscriber section.

**URL** : `/api/profile/:id/subscriber`
** id : current logined User Id **

**Method** : `PUT`

**Auth required** : `YES`

**Header**  : `Authorization:{jwt-token}`


| Param       |Require |Type     | Description     | 
| :------------- |  :-----------|  :----------- |----------- |
|  subscriberPrice |Yes|  Number    | subscriberPrice of current User.|

** Error Responses: **

**Condition** : subscriberPrice of current user is null

**Code** : `400 BAD REQUEST`

* Content example

```json
{
    "err": "Cannot read property 'subscriberPrice' of null"
}
```

** Success Response: **

**Code** : `200 success`

* Resonse example 


```json
{
    "subscriberPrice": 500,
    "_id": "61c406e500ee9c2964b8c7fc",
    "username": "steven",
    "email": "Whitehorse@gmail.com",
    "password": "$2a$10$zsgwPUzldThHrsTvARJ0Uurb7d4rHu4BaWf4CCw.8rQm0KkJll2Za",
    "role": "viewer",
    "birth": "1910-12-12T01:00:00.000Z",
    "viewerAge": "18",
    "IDType": "passport",
    "IDFront": "1640236772969.png",
    "IDBack": "1640236772971.png",
    "CategoryType": "music",
    "date": "2021-12-23T05:19:33.250Z",
    "__v": 0
}
```

# Change Password

Change password of current User on AccountSetting section.

**URL** : `/api/profile/:id/accountSetting`
** id : current user id **

**Method** : `PUT`

**Auth required** : `YES`

| Param       |Require |Type     | Description     | 
| :------------- |  :-----------|  :----------- |----------- |
|  password |Yes|  String    | Current logined user id.|

**Header**  : `Authorization:{jwt-token}`


** Success Response: **

**Code** : `200 success`

* Resonse example 

```json
{
    "changePassword": {
        "subscriberPrice": 0,
        "_id": "61c3ccfbaa10e627e8b603ca",
        "email": "kungfu@gmail.com",
        "password": "123123123",
        "role": "creator",
        "birth": "1910-12-12T01:00:00.000Z",
        "viewerAge": "18",
        "IDType": "passport",
        "IDFront": "1640231433440.png",
        "IDBack": "1640221947243.png",
        "CategoryType": "music",
        "date": "2021-12-23T01:12:27.591Z",
        "__v": 0
    }
}
```

# Delete account

Delete account of current user on Account Setting section.

**URL** : `/api/profile/:id/accountSetting`
** id : current logined user id **

**Method** : `DELETE`

**Auth required** : `YES`

| Param       |Require |Type     | Description     | 
| :------------- |  :-----------|  :----------- |----------- |
|  password |Yes|  String    | Current logined user id.|

**Header**  : `Authorization:{jwt-token}`

** Error Responses: **

**Condition** : If password of current user is wrong, like this msg

**Code** : `400 BAD REQUEST`

* Content example

```json
{
    "message": "errror",
    "erroMessage": "password is not match"
}
```

** Success Response: **

**Code** : `200 success`

* Resonse example 

```json
{
    "success": true
}
```

# Switch Account

Swtch account of current user on Account Setting section.

**URL** : `/api/profile/:id/switchAccount`
** id : current logined user id **

**Method** : `PUT`

**Auth required** : `YES`

**Header**  : `Authorization:{jwt-token}`


** Success Response: **

**Code** : `200 success`

* Resonse example 

```json
{
    "switchAccount": {
        "subscriberPrice": 0,
        "_id": "61c406e500ee9c2964b8c7fc",
        "username": "steven",
        "email": "Whitehorse@gmail.com",
        "password": "$2a$10$zsgwPUzldThHrsTvARJ0Uurb7d4rHu4BaWf4CCw.8rQm0KkJll2Za",
        "role": "viewer",
        "birth": "1910-12-12T01:00:00.000Z",
        "viewerAge": "18",
        "IDType": "passport",
        "IDFront": "1640236772969.png",
        "IDBack": "1640236772971.png",
        "CategoryType": "music",
        "date": "2021-12-23T05:19:33.250Z",
        "__v": 0
    }
}
```

# Buy UveCoin

Bye UveCoin by viewer on Financials section.

**URL** : `/api/profile/:id/getUveCoin`
** id : current logined Viewer Id **

**Method** : `POST`

**Auth required** : `YES`

| Param       |Require |Type     | Description     | 
| :------------- |  :-----------|  :----------- |----------- |
|  coinAmount |Yes|  String    | Current logined user id.|

**Header**  : `Authorization:{jwt-token}`


** Success Response: **

**Code** : `200 success`

* Resonse example 


```json
{
    "_id": "61c40d2a00ee9c2964b8c811",
    "viewId": "61c406e500ee9c2964b8c7fc",
    "coinAmount": 500,
    "date": "2021-12-23T05:46:18.036Z",
    "__v": 0
}
```

# Get UveCoin

Get UveCoin by viewer on Financials section.

**URL** : `/api/profile/:id/getUveCoin`
** id : current logined Viewer Id **

**Method** : `GET`

**Auth required** : `YES`

**Header**  : `Authorization:{jwt-token}`


** Success Response: **

**Code** : `200 success`

* Resonse example 


```json
[
    {
        "_id": "61c3679594cc5027e808952f",
        "viewId": "61c362c6f6fca119a498b1d1",
        "coinAmount": 500,
        "date": "2021-12-22T17:59:49.276Z",
        "__v": 0
    },
    {
        "_id": "61c3679794cc5027e8089531",
        "viewId": "61c362c6f6fca119a498b1d1",
        "coinAmount": 500,
        "date": "2021-12-22T17:59:51.674Z",
        "__v": 0
    },
    {
        "_id": "61c40d2a00ee9c2964b8c811",
        "viewId": "61c406e500ee9c2964b8c7fc",
        "coinAmount": 500,
        "date": "2021-12-23T05:46:18.036Z",
        "__v": 0
    }
]
```

# Transiction History

Get payment history.

**URL** : `/api/profile/:id/getTransictionHistory`
** id : current logined user Id **

**Method** : `GET`

**Auth required** : `YES`

**Header**  : `Authorization:{jwt-token}`


** Success Response: **

**Code** : `200 success`

* Resonse example 


```json
[
    {
        "tips": [],
        "coinAmounts": [],
        "_id": "61c3678c94cc5027e808952d",
        "creatorId": "61c3675d94cc5027e8089525",
        "viewId": "61c362c6f6fca119a498b1d1",
        "subscribePrice": 200,
        "date": "2021-12-22T17:59:40.373Z",
        "__v": 0
    },
    {
        "tips": [],
        "coinAmounts": [],
        "_id": "61c40cf500ee9c2964b8c80f",
        "creatorId": "61c3675d94cc5027e8089525",
        "viewId": "61c406e500ee9c2964b8c7fc",
        "subscribePrice": 200,
        "date": "2021-12-23T05:45:25.531Z",
        "__v": 0
    }
]
```

# Stripe payment

**URL** : `/api/profile/stripeInternet`

**Method** : `POST`
**Auth required** : `YES`

**Header** : `Authorization:{jwt-token}`

| Param       |Require |Type     | Description     | 
| :------------- |  :-----------|  :----------- |----------- |
|  amount |Yes|  Number    | pay amount of current viewer.|
|  currency |Yes|  String    | kind of Dallar.|
|  description |Yes|  String    | pay description by current viewer.|
|  name |Yes|  String    | Name of current viewer.|
|  email |Yes|  String    | Email of current viewer.|
|  token |Yes|  String    | Token of current payment.|

**Condition** : Internal Server Error.

**Code** : `500`

* Resonse example 

```json
{
    "msg": "Internal Server error"
}
```