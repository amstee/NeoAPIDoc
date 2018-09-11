# Update circle informations
**[HOME](../README.md)**

**URL** : `/circle/update`

**Method** : `PUT`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device


Informations to provide :

```json
{
    "device_token | token": "[JWT token]",
    "circle_id": "[integer]",
    "name": "[string(120)]"
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

**Condition** : Specified circle was not found.

**Code** : `404 NOT FOUND`

**Content example**

```json
{
    "message": "[Error message]",
    "success": false
}
```

### OR

**Condition** : You do not have access to this circle.

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