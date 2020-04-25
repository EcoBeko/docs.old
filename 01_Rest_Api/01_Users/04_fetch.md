# api/users/fetch/:phone (GET)

## Description

Fetch user data by the given :phone url parameter

|    Note    | Value |
| :--------: | :---: |
| Need Token |  Yes  |
| Test route |  No   |

## Request example

| Parameter | Description                                            |
| :-------: | ------------------------------------------------------ |
|   phone   | Following Kazakhstan's phone pattern (omitting prefix) |

```HTTP
https://domain.name/api/users/fetch/7086144672
```

## Response examples

| Response Status code | Description         |
| :------------------: | ------------------- |
|         200          | Success             |
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

### User doesn't exists

HTTP code: 404

```js
{
  status: false,
  message: "User does not exists"
}
```
