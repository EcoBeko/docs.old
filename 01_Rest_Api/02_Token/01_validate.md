# api/token/validate (GET)

## Description

Create a new post

|    Note    | Value |
| :--------: | :---: |
| Need Token |  No   |
| Test route |  No   |

## Request example

| Parameter | Description |
| :-------: | ----------- |
|   token   | Text        |

```js
{
  token: "token-string",
}
```

## Response examples

| Response Status code | Description                    |
| :------------------: | ------------------------------ |
|         202          | Valid                          |
|         406          | Validation failed              |
|         412          | Request conditions are not met |

### Created

HTTP code: 202

```js
{
  status: true,
  message: "Token is Valid"
}
```

### Validation failed

HTTP code: 406

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
