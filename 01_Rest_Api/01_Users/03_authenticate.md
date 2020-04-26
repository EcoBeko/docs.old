# api/users/authenticate (GET)

## Description

Validate user credentials and send access token

|    Note    | Value |
| :--------: | :---: |
| Need Token |  No   |
| Test route |  No   |

## Request example

| Parameter | Description                                                    |
| :-------: | -------------------------------------------------------------- |
|   phone   | String, Following Kazakhstan's phone pattern (omitting prefix) |
| password  | String, user's password                                        |

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
|         400          | Phone number exists            |
|         406          | Validation error               |
|         412          | Request conditions are not met |

### 200 - Success

```js
{
  status: true,
  message: "Token created",
  token: "token-string"
}
```

### 400 - Phone number exists

```js
{
  status: false,
  message: "Phone number already exists"
}
```

### 406 - Validation error

```js
{
  status: false,
  message: "Data validation error"
}
```

### 412 - Request conditions are not met

```js
{
  status: false,
  message: "Request conditions are not met"
}
```
