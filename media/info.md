# Media info
**[HOME](../README.md)**

**URL** : `/media/info/<media_id>`

**Method** : `GET`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device & Access to the media

**Description :**
Get a media informations

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
    "content": {
        "id": "[integer]",
        "filename": ["string"],
        "extension": "[string]",
        "identifier": "[string]",
        "uploaded": "[string]"
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