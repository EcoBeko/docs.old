# api/posts/fetch-portion (GET)

## Description

Fetch limited amount of posts

|    Note    |  Value  |
| :--------: | :-----: |
| Need Token | **Yes** |
| Test route |   No    |

## Request example

| Parameter | Description             |
| :-------: | ----------------------- |
|  offset   | Fetch offset, default 0 |

```js
{
  offset: 3,
}
```

## Response examples

| Response Status code | Description                     |
| :------------------: | ------------------------------- |
|         204          | No rows left                    |
|         206          | Success                         |
|         401          | No token presented              |
|         403          | Token presented, but is invalid |

### Created

HTTP code: 204

```js
{
  status: true,
  message: "No rows left"
  posts: []
}
```

### Success

HTTP code: 206

```js
{
  status: true,
  message: "Success",
  posts: [
    // data
  ]
}
```

### Unauthorized

HTTP code: 401

```js
{
  status: false,
  message: "No token presented"
}
```

### Token is invalid

HTTP code: 403

```js
{
  status: false,
  message: "Bad token"
}
```
