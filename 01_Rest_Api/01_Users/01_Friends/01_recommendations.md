# api/users/friends/recommendations (GET)

## Description

Get friends recommendations for user

|    Note    |  Value  |
| :--------: | :-----: |
| Need Token | **Yes** |
| Test route |   No    |

## Response examples

| Response Status code | Description                      |
| :------------------: | -------------------------------- |
|         204          | No close friends, random is used |
|         206          | Success                          |
|         401          | No token presented               |
|         403          | Token presented, but is invalid  |

### Created

HTTP code: 204

```js
{
  status: true,
  message: "No close friends"
  users: [
    // random users
    {
      name: "user-name",
      surname: "user-surname",
      phone: "user-phone",
      avatar: "user-avatar",
    }
  ]
}
```

### Success

HTTP code: 206

```js
{
  status: true,
  message: "Success",
  users: [
    // closely related users
    {
      name: "user-name",
      surname: "user-surname",
      phone: "user-phone",
      avatar: "user-avatar",
    }
  ]
}
```

### Unauthorized

HTTP code: 401

```js
{
  status: false,
  message: "No token presented"
}
```

### Token is invalid

HTTP code: 403

```js
{
  status: false,
  message: "Bad token"
}
```
