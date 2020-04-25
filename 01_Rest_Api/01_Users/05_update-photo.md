# api/users/update-photo (PUT)

## Description

Update user's avatar

|    Note    |  Value  |
| :--------: | :-----: |
| Need Token | **Yes** |
| Test route |   No    |

## Request example

| Parameter | Description                |
| :-------: | -------------------------- |
|  avatar   | Hash sum of the new avatar |

```js
{
  avatar: "some-avatar",
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
  message: "Relationship updated"
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
