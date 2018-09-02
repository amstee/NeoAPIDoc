# Web Sockets
**[HOME](../README.md)**

This is the web sockets documentation which will detail the handlers, how to access them, their parameters and returns.

### Library

https://flask-socketio.readthedocs.io/en/latest/
 
### Basics

**Connection :**

Simple socket oppening, allows the server to store the sid (socket id).

```html
<script type="text/javascript" src="//cdnjs.cloudflare.com/ajax/libs/socket.io/1.3.6/socket.io.min.js"></script>
    <script type="text/javascript" charset="utf-8">
    var socket = io.connect('https://' + document.domain + ':' + location.port);
</script>
```

**Authentication :**

Send a request on the "authenticate" channel : `@socketio.on('authenticate')`.<br/>
The request must have a json content with the key "token" and the Json Web Token associated to the user *(Same thing for the device)*.<br/>
If an error occur, a message will be sent on the "error" channel otherwise a message wil be sent ont the channel "success".

**Disconnect :**

Simple request on the "disconnect" channel, no parameters required

### Listened Channels

Each channel that ask for one or more parameters systematically send a message on the channels "error" or "success".

Name | Parameters | Details
:---: | :---: | :---:
connect | `-` | -
authenticate | `token` | JWT
disconnect | `-` | -
join_conversation | `conversation_id` | ID of the conversation
leave_conversation | `conversation_id` | ID of the conversation
join_circle | `circle_id` | ID of the circle
leave_circle | `circle_id` | ID of the circle
message | **Mendatory:** `conversation_id`<br/>**Optional:** `text_message, files` | **Mendatory:** ID of the conversation <br/> **Optional:** <br/> text_message --> message<br/>files --> file list<br/>`Example: [file.txt, ...]`
writing | `conversation_id, is_writing` | ID of the conversation, Boolean
webrtc_credentials | `-` | Return the username and password for the `turn server` connection on the channel `webrtc_config`
webrtc_stun_info | `-` | Return the STUN servers info on the `webrtc_config` channel
webrtc_turn_info | `-` | Return the TURN servers info on the `webrtc_config` channel
webrtc_forward | `email OR user_id OR device_id` | Forward a message under the JSON format to a user

### Circle Events

Each json contains the circle id. Example : <br/>
```python
json = {"event": "join", "user": "example"} 
json["circle_id"] = 0
```

Description | Channel | JSON
:---: | :---: | :---:
invitation | circle_invite | `{'event': 'invite', 'circle_id': circle.id} `
user join circle | circle | `{'event': 'join', 'user': link.user.email}`
user leave circle | circle | `{'event': 'quit', 'user': link.user.email}`
kick user | circle | `{'event': 'kick', 'user': kick.email, 'from': user.email}`
circle info modified | circle | `{'event': 'update'}`
user from circle connect | circle | `{'event': 'connect', 'user': user.email}`
user from circle disconnect | circle | `{'event': 'disconnect', 'user': data.email}`
device info from circle modified | circle | `{'event': 'device', 'type': 'update', 'device_id': device.id}`
device connect | circle | `{'event': 'device', 'type': 'connect', 'device_id': device.id}`
device disconnect | circle | `{'event': 'device', 'type': 'disconnect', 'device_id': data.id}`

### Conversations Events

Each json contains the conversation id.

Description | Channel | JSON
:---: | :---: | :---:
info update | conversation | ``
invite | conversation | ``
user promotion | conversation | ``
user kick | conversation | ``
user quit | conversation | ``
add device | conversation | ``
remove device | conversation | ``

### Messages Events

Description | Channel | JSON
:---: | :---: | :---:
message sent to a conversation | message | `'conversation_id': conv.id, 'message': message.getSimpleContent(), 'time': message.sent, 'sender': socket.client.getSimpleContent(), 'media_list': media_list, 'status': 'done'}` OR `{'conversation_id': conv.id, 'message': message.getSimpleContent(), 'status': 'pending'}`
message deletion | message | `{"conversation_id": conv_id, "message_id": id, "event": 'delete'}`
message update | message | `{"conversation_id": message.conversation_id, "message_id": message.id, "event": 'update'}`
user write | writing | `{'conversation_id': json['conversation_id'], 'device': False, 'user': socket.client.email, 'is_writing': json['is_writing']}` OR `{'conversation_id': json['conversation_id'], 'device': True, 'is_writing': json['is_writing']}`

### Medias Events

Description | Channel | JSON
:---: | :---: | :---:
If a message is sent through websocket and need medias to be uploaded | media | `{'media_list': media_list, 'message_id': message.id}`

### Events Webrtc

Description | Channel | JSON
:---: | :---: | :---:
Turn servers config | webrtc_config | `TURN = [{"domain": "webrtc.neo.ovh", "ip": "", "port": 3478}]`
Stun servers config | webrtc_config | `STUN = [{"domain":"webrtc.neo.ovh","ip": "", "port": 3478,}]`
Credentials for user connection to turn servers | webrtc_config | `{"username": username, "password": password}`
Message sent from another user | webrtc_config | `{ "sender_id": socket.client.id, "is_device": socket.client.is_device, "content": json}`

