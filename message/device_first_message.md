# First message (as Device)
**[HOME](../README.md)**

**URL** : `/device/message/first-message`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : Device


Informations to provide :

```json
{
    "device_token": "[string]",
    "email": "[string(120)]",
    "text_message": "[string(8192)]",
    "files": "[list]"
}
```

* *Not mandatory

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
    "message_id": "[integer]",
    "media_list":   [{
                        "id": "[integer]",
                        "filename": "[string(120)]",
                        "extension": "[string(120)]",
                        "identifier": "[string(10)]",
                        "uploaded": "[boolean]"
                    }],
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