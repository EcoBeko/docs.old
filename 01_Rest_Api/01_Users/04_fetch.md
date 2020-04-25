# api/users/fetch (GET)

## Description

Fetch user data by the given. User's info will be held in token

|    Note    |  Value  |
| :--------: | :-----: |
| Need Token | **Yes** |
| Test route |   No    |

## Response examples

| Response Status code | Description         |
| :------------------: | ------------------- |
|         200          | Success             |
|         401          | No token presented  |
|         403          | Bad token           |
|         404          | User doesn't exists |

### Created

HTTP code: 200

```js
{
  status: true,
  message: "Token created",
  user: {
    name: "user-name",
    surname: "user-surname",
    role: "user-role",
    gender: 1,
    phone: "user-phone",
    avatar: "user-avatar",
    birthday: "user-birthday",
    stats: {
      trees: 0.0,
      energy: 0.0,
      waste: 0.0
    }
  }
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

### User doesn't exists

HTTP code: 404

```js
{
  status: false,
  message: "User does not exists"
}
```
