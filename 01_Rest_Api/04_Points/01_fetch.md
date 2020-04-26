# api/points/fetch/:type (GET)

## Description

Get points by their type (recycle, utilization)

|    Note    | Value |
| :--------: | :---: |
| Need Token |  No   |
| Test route |  No   |

## Request example

| Parameter | Description               |
| :-------: | ------------------------- |
|   query   | Array of waste types ids' |

```js
{
  query: [
    2, 3, 4
  ],
}
```

## Response examples

| Response Status code | Description                    |
| :------------------: | ------------------------------ |
|         200          | Success                        |
|         204          | No content                     |
|         412          | Request conditions are not met |

### Success

HTTP code: 200

```js
{
  status: true,
  message: "Success"
  points: [
    // query result
    {
      id: 1,
      title: "point-title",
      address: "point-address",
      workingTime: "point-workingTime",
      site: "point-site",
      type: "point-type",
      phone: "point-phone",
      additionalInfo: "point-additionalInfo",
    }
  ]
}
```

### No Content

HTTP code: 204

```js
{
  status: true,
  message: "No Content"
  points: [
    // no results
  ]
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
