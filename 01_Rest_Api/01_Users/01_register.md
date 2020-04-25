# api/users/register (POST)

## Description

Register a new user

|    Note    | Value |
| :--------: | :---: |
| Need Token |  No   |
| Test route |  No   |

## Request example

| Parameter | Description                                            |
| :-------: | ------------------------------------------------------ |
|   name    | User's name                                            |
|  surname  | User's surname                                         |
|   role    | User's role                                            |
| password  | User's password                                        |
|  gender   | 1 for male, 0 for female                               |
|   phone   | Following Kazakhstan's phone pattern (omitting prefix) |
| birthday  | Only date in format DD-MM-YYYY                         |

```js
{
  name: "Ansar",
  surname: "Ryspekov",
  role: "user",
  password: "some-password",
  gender: 1,
  phone: "7086144672",
  birthday: "19-01-2001"
}
```

## Response examples

| Response Status code | Description                    |
| :------------------: | ------------------------------ |
|         201          | Created                        |
|         400          | Phone number exists            |
|         406          | Validation error               |
|         412          | Request conditions are not met |

### Created

HTTP code: 201

```js
{
  status: true,
  message: "User created"
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

HTTP code: 406

```js
{
  status: false,
  message: "Data validation error"
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
