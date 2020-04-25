# api/users/friends/fetch (GET)

## Description

Fetch user's friends list

|    Note    |  Value  |
| :--------: | :-----: |
| Need Token | **Yes** |
| Test route |   No    |

## Response examples

| Response Status code | Description              |
| :------------------: | ------------------------ |
|         200          | Success                  |
|         401          | No Token                 |
|         403          | Unauthorized (bad token) |

### Created

HTTP code: 201

```js
{
  status: true,
  message: "Success",
  users: [
    // all user's friends
    {
      phone: "user-phone",
      name: "user-name",
      surname: "user-surname",
      avatar: "user-avatar",
      lastTime: "dd-mm-yyyy h:min:sec",
      status: "relationship-status"
    }
  ]
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
