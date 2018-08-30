# Create message (As admin, As device)
**[HOME](../README.md)**

**URL** : `/admin/device/message/create`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : Admin, Device


Informations to provide :

```json
{
    "token": "[JWT token]",
    "device_id": "[integer]",
    "conversation_id": "[integer]",
    "text": "[string(8192)]",
    "directory_name": "string(50)",
    *"files": "[undefined]"
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