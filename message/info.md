# Message informations

**URL** : `/message/info`

**Method** : `POST`

**Authentication required** : YES (JWT token)

**Permissions required** : User


Informations to provide :

```json
{
    "token": "[JWT token]",
    "message_id": "[integer]"
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
                    "medias":   [
                                    media.get_content() for media in self.media_links
                                ]
                },
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