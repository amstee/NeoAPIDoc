# Delete cirle
**[HOME](../README.md)**

**URL** : `/admin/circle/delete`

**Method** : `DELETE`

**Authentication required** : YES (JWT token)

**Permissions required** : Admin


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
    "content": {
                "id": "[integer]",
                "name": "[string(120)]",
                "created": "[datetime]",
                "updated": "[datetime]",
                "device": "[integer]",
               },
    "success": True
}
```

## Error Responses

**Condition** : Circle not found.

**Code** : `404 NOT FOUND`

**Content example**

```json
{
    "message": "Le cercle est introuvable",
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
