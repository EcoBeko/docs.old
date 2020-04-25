# api/users/authenticate (POST)

## Description

Validate user credentials and send access token

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

| Response Status code | Description                             |
| :------------------: | --------------------------------------- |
|         200          | Success                                 |
|         400          | Phone number exists or validation error |
|         412          | Request conditions are not met          |

### Created

HTTP code: 200

```js
{
  status: true,
  message: "Token created",
  token: "token-string"
}
```

### Phone number exists

HTTP code: 400

```js
{
  status: false,
  message: "Phone number already exists"
}
```

### Validation error

HTTP code: 400

```js
{
  status: false,
  message: "Data validation error"
}
```
