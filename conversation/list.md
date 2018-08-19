# List conversation

**URL** : `/conversation/kick`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User


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
    "content":  {
                    "id": "[integer]",
                    "name": "[string(120)]",
                    "created": "[datetime]",
                    "updated": "[datetime]",
                    "circle_id": "[integer]",
                    "device_access": "[boolean]"
                },
    "success": True
}
```

## Error Responses

**Condition** : No right in specified circle.

**Code** : `403 FORBIDDEN`

**Content example**

```json
{
    "message": "[Error message]",
    "success": False
}
```

### OR

**Condition** : Error occured.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "message": "[Error message]",
    "success": False
}
```