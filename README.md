# NEO API documentation

This is the api documentation which will detail the available route, how to access them, their parameters and answers.

### Account related

Endpoints for viewing, manipulating and creating accounts that users have access to.

* [Create account](account/create.md) : `POST /account/create`
* [Log in account](account/login.md) : `POST /account/login`
* [Log out account](account/logout.md) : `POST /account/logout`
* [Account informations](account/info.md) : `POST /account/info`
* [Modify account informations](account/modify.md) : `POST /account/modify`
* [Check email availability](account/create_available.md) : `POST /account/create/available`
* [Modify account password](account/modify_password.md) : `POST /account/modify/password`
* [Verify account token validity](account/token.md) : `POST /token/verify`
* [Promote account](account/promote.md) : `POST /admin/account/promote`
* [Account information (as device)](account/device_info.md) : `POST /device/account/info`