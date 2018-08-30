# List messages

**URL** : `/device/message/list`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : Device


Informations to provide :

```json
{
    "token": "[JWT token]",
    "conversation_id": "[integer]",
    "quantity": "[integer]"
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
    "content":  [{
                    "id": "[integer]",
                    "link": {
                        "id": "[integer]",
                        "created": "[datetime]",
                        "updated": "[datetime]",
                        "privilege": "[string(10)]",
                        "user_id": "[integer]",
                        "conversation_id": "[integer]",
                        "circle_id": "[integer]"
                    },
                    "sent": "[boolean]",
                    "read": "[boolean]",
                    "content": "[string(8192)]",
                    "medias":   [{
                        "id": "[integer]",
                        "filename": ["string"],
                        "extension": "[string]",
                        "identifier": "[string]",
                        "uploaded": "[string]"
                        }
                    ]
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