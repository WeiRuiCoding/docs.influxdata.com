---
title: string() function
description: The `string()` function converts a single value to a string.
menu:
  flux_0_36:
    name: string
    parent: built-in-type-conversions
weight: 2
---

The `string()` function converts a single value to a string.

_**Function type:** Type conversion_  
_**Output data type:** String_

```js
string(v: 123456789)
```

## Parameters

### v
The value to convert.

## Examples
```js
from(bucket: "sensor-data")
  |> filter(fn:(r) =>
    r._measurement == "system" and
  )
  |> map(fn:(r) => ({ r with model_number string(v: r.model_number) }))
```
