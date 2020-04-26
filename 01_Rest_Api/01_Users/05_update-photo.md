# api/users/update-photo (PUT)

## Description

Update user's avatar

|    Note    |  Value  |
| :--------: | :-----: |
| Need Token | **Yes** |
| Test route |   No    |

## Request example

| Parameter | Description                        |
| :-------: | ---------------------------------- |
|  avatar   | String, hash sum of the new avatar |

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
|         403          | Unauthorized                   |
|         412          | Request conditions are not met |

### 200 - Updated

```js
{
  status: true,
  message: "Avatar updated"
}
```

### 401 - No token

```js
{
  status: false,
  message: "No token presented"
}
```

### 403 - Unauthorized

```js
{
  status: false,
  message: "Bad token"
}
```

### 412 - Request conditions are not met

```js
{
  status: false,
  message: "Request conditions are not met"
}
```
