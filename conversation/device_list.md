# List conversation (as Device)
**[HOME](../README.md)**

**URL** : `/device/conversation/list`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : Device


Informations to provide :

```json
{
    "token": "[JWT token]",
    "circle_id": "[integer]"
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
    "success": True
}
```

## Error Responses

**Condition** : Error occured.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "message": "[Error message]",
    "success": False
}
```