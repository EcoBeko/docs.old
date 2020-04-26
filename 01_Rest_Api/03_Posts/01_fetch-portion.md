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
|         412          | Request conditions are not met  |

### 204 - No rows

```js
{
  status: true,
  message: "No rows left"
  posts: []
}
```

### 206 - Success

```js
{
  status: true,
  message: "Success",
  posts: [
    // data
    {
      title: "post-title",
      article: "post-article",
      owner: {
        name: "owner-name",
        surname: "owner-surname",
        avatar: "owner-avatar",
      },
      likes: 0,
      image: "post-image",
      time: "post-time"
    }
  ]
}
```

### 401 - No Token

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
