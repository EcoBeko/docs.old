# api/posts/fetch-one/:post-id (GET)

## Description

Fetch single post by it's id

|    Note    |  Value  |
| :--------: | :-----: |
| Need Token | **Yes** |
| Test route |   No    |

## Request example

| Parameter | Description |
| :-------: | ----------- |
|  post-id  | Post's id   |

```http
http://domain.name/api/posts/fetch-one/123
```

## Response examples

| Response Status code | Description |
| :------------------: | ----------- |
|         200          | Success     |
|         404          | Not-found   |

### Success

HTTP code: 200

```js
{
  status: true,
  message: "Success"
  post: {
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
}
```

### Not found

HTTP code: 404

```js
{
  status: false,
  message: "Post not found"
}
```
