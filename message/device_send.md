# Send message (as Device)
**[HOME](../README.md)**

**URL** : `/device/message/send`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : Device


Informations to provide :

```json
{
    "token": "[JWT token]",
    "conversation_id": "[integer]",
    "text_message": "[string(8192)]",
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