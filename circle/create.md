# Create cirle
**[HOME](../README.md)**

**URL** : `/circle/create`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User


Informations to provide :

```json
{
    "token": "[JWT token]",
    "name": "[string(120)]"
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
    "content": {
                "id": "[integer]",
                "name": "[string(120)]",
                "created": "[datetime]",
                "updated": "[datetime]",
                "device": "[integer]"
               },
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