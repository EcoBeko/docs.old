# api/users/validate (POST)

## Description

Validates user credentials

|    Note    | Value |
| :--------: | :---: |
| Need Token |  No   |
| Test route |  No   |

## Request example

| Parameter | Description                                                    |
| :-------: | -------------------------------------------------------------- |
|   phone   | String, following Kazakhstan's phone pattern (omitting prefix) |
| password  | String, User's password                                        |

```js
{
  phone: "7086144672",
  password: "some-password"
}
```

## Response examples

| Response Status code | Description                    |
| :------------------: | ------------------------------ |
|         200          | Success                        |
|         404          | User doesn't exists            |
|         406          | Incorrect password             |
|         412          | Request conditions are not met |

### 200 - Success

```js
{
  status: true,
  message: "Credentials are valid"
}
```

### 404 - User doesn't exists

```js
{
  status: false,
  message: "User does not exists";
}
```

### 406 - Incorrect password

```js
{
  status: false,
  message: "Password is incorrect"
}
```

### 412 - Request conditions are not met

```js
{
  status: false,
  message: "Request conditions are not met"
}
```
