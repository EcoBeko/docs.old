# api/users/update-credentials (PUT)

## Description

Update user's password

|    Note    |  Value  |
| :--------: | :-----: |
| Need Token | **Yes** |
| Test route |   No    |

## Request example

|  Parameter  | Description           |
| :---------: | --------------------- |
| oldPassword | Old password to check |
| newPassword | New password to set   |

```js
{
  oldPassword: "some-old-password",
  newPassword: "some-new-password",
}
```

## Response examples

| Response Status code | Description                    |
| :------------------: | ------------------------------ |
|         200          | Updated                        |
|         400          | Old password is incorrect      |
|         401          | No Token                       |
|         403          | Unauthorized (bad token)       |
|         412          | Request conditions are not met |

### Updated

HTTP code: 200

```js
{
  status: true,
  message: "User's info updated"
}
```

### Password is incorrect

HTTP code: 400

```js
{
  status: false,
  message: "Incorrect password"
}
```

### No token

HTTP code: 401

```js
{
  status: false,
  message: "No token presented"
}
```

### Unauthorized

HTTP code: 403

```js
{
  status: false,
  message: "Bad token"
}
```

### Request conditions are not met

HTTP code: 412

```js
{
  status: false,
  message: "Request conditions are not met"
}
```
