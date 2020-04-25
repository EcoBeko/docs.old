# api/users/validate (POST)

## Description

Validates user credentials

|    Note    | Value |
| :--------: | :---: |
| Need Token |  No   |
| Test route |  No   |

## Request example

| Parameter | Description                                            |
| :-------: | ------------------------------------------------------ |
|   phone   | Following Kazakhstan's phone pattern (omitting prefix) |
| password  | User's password                                        |

```js
{
  phone: "7086144672",
  password: "some-password"
}
```

## Response examples

| Response Status code | Description                               |
| :------------------: | ----------------------------------------- |
|         204          | Success                                   |
|         406          | Incorrect password or user doesn't exists |

### Success

HTTP Code: 204

```js
// no content
```

### Incorrect password

HTTP Code: 406

```js
{
  error: "Password is incorrect"
}
```

### User doesn't exists

HTTP Code: 406

```js
{
  error: "User does not exists"
}
```
