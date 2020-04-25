# api/posts/write (POST)

## Description

Create a new post

|    Note    |  Value  |
| :--------: | :-----: |
| Need Token | **Yes** |
| Test route |   No    |

## Request example

| Parameter | Description      |
| :-------: | ---------------- |
|   title   | Text             |
|  article  | Long Text        |
|   image   | Image's hash sum |

```js
{
  title: "some-title",
  article: "some-article",
  image: "some-image",
}
```

## Response examples

| Response Status code | Description                     |
| :------------------: | ------------------------------- |
|         201          | Created                         |
|         401          | No token presented              |
|         403          | Token presented, but is invalid |
|         406          | Validation failed               |
|         412          | Request conditions are not met  |

### Created

HTTP code: 201

```js
{
  status: true,
  message: "Article created"
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

### Validation failed

HTTP code: 406

```js
{
  status: false,
  message: "Some-fields have failed the validation"
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
