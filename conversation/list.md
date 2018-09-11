# List conversation
**[HOME](../README.md)**

**URL** : `/conversation/list/<circle_id>`

**Method** : `GET`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device & Being member of the circle


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
            "circle_id": "[integer]",
            "device_access": "[boolean]"
        }
    ],
    "success": true
}
```

## Error Responses

**Condition** : No right in specified circle.

**Code** : `403 FORBIDDEN`

**Content example**

```json
{
    "message": "[Error message]",
    "success": false
}
```

### OR

**Condition** : Error occured.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "message": "[Error message]",
    "success": false
}
```