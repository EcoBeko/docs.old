# api/users/stats/add (PUT)

## Description

Update user statistics

|    Note    |  Value  |
| :--------: | :-----: |
| Need Token | **Yes** |
| Test route |   No    |

## Request example

| Parameter | Description            |
| :-------: | ---------------------- |
|   trees   | Amount of saved trees  |
|  energy   | Amount of saved energy |
|   waste   | Miscellaneous rubbish  |

```js
{
  trees: 0.1,
  energy: 0.5,
  waste: 0.3
}
```

## Response examples

| Response Status code | Description                     |
| :------------------: | ------------------------------- |
|         202          | Added                           |
|         401          | No token presented              |
|         403          | Token presented, but is invalid |
|         412          | Request conditions are not met  |

### Added

HTTP code: 202

```js
{
  status: true,
  message: "Added"
}
```

### No token presented

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
  message: "Bad Token"
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
