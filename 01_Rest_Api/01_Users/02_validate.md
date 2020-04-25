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
|         412          | Request conditions are not met            |

### Success

HTTP Code: 204

```js
{
  status: true,
  message: "Credentials are valid"
}
```

### Incorrect password

HTTP Code: 406

```js
{
  status: false,
  message: "Password is incorrect"
}
```

### User doesn't exists

HTTP Code: 406

```js
{
  status: false,
  message: "User does not exists";
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
