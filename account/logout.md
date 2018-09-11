# Log out from Account
**[HOME](../README.md)**

Log out from account (invalidating JWT token).

**URL** : `/account/logout`

**Method** : `POST`

**Authentication required** : YES (token)

**Permissions required** : User


Informations to provide :

```json
{
    "token": "[JWT token]"
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
    "success": true
}
```

## Error Responses

**Condition** : Error occured.

**Code** : `401 UNAUTHORIZED`

**Content example**

```json
{
    "message": "[Error message]",
    "success": false
}
```