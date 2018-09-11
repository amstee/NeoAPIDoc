# Checking email availability
**[HOME](../README.md)**

Checking email availability.

**URL** : `/email/available/<email>`

**Method** : `GET`

**Authentication required** : NO

**Permissions required** : None


Informations to provide :

```json
{
    "email": "string(128)"
    
}
```

## Success Response

**Condition** : If email is available.

**Code** : `200 OK`

**Content example**

```json
{
    "success": true
}
```

### OR

**Condition** : If email is unavailable.

**Code** : `200 OK`

**Content example**

```json
{
    "success": false
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