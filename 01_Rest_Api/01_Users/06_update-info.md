# api/users/update (PUT)

## Description

Update user's info

|    Note    |  Value  |
| :--------: | :-----: |
| Need Token | **Yes** |
| Test route |   No    |

## Request example

| Parameter | Description               |
| :-------: | ------------------------- |
|   name    | User's name               |
|  surname  | User's surname            |
|  gender   | 1 for male, 0 for female  |
| birthday  | Date in format dd-mm-yyyy |

```js
{
  name: "user-name",
  surname: "user-surname",
  gender: "user-gender",
  birthday: "user-birthday",
}
```

## Response examples

| Response Status code | Description                    |
| :------------------: | ------------------------------ |
|         200          | Updated                        |
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
