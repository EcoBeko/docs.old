# api/users/friends/update (PUT)

## Description

Update relationship status with friend

|    Note    |  Value  |
| :--------: | :-----: |
| Need Token | **Yes** |
| Test route |   No    |

## Request example

| Parameter | Description                                                                  |
| :-------: | ---------------------------------------------------------------------------- |
|   phone   | Following Kazakhstan's phone pattern (omitting prefix). Friends phone number |

```js
{
  phone: "7086144672",
}
```

## Response examples

| Response Status code | Description                    |
| :------------------: | ------------------------------ |
|         200          | Updated                        |
|         401          | No Token                       |
|         403          | Unauthorized (bad token)       |
|         404          | Phone number not exists        |
|         412          | Request conditions are not met |

### Updated

HTTP code: 200

```js
{
  status: true,
  message: "Relationship updated"
}
```

### Phone number doesn't exists

HTTP code: 400

```js
{
  status: false,
  message: "Phone number does not exists"
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
