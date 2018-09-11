# List circles
**[HOME](../README.md)**

**URL** : `/user/circle/list`

**Method** : `GET`

**Authentication required** : YES (JWT token)

**Permissions required** : User


Informations to provide in header :

```json
{
    "Authorization": "[string]"
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
    "content": [
        {
            "id": "[integer]",
            "name": "[string(120)]",
            "created": "[datetime]",
            "updated": "[datetime]",
            "device": "[integer]"
        }
    ],
    "success": true
}
```

## Error Responses

**Condition** : Error occured.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "message": "[Error message]",
    "success": false
}
```