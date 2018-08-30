# Admin media info

**URL** : `/admin/media/info`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : Admin

**Description :**
Get any media informations

Informations to provide :

```json
{
  "media_id": "[integer]"
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
        "uploaded": "[string]",
        "media_link": "[string]",
        "link_content": "[dictionnary]",
        "directory": "[string]"
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