# server-timing

This module adds [Server-Timing](https://www.w3.org/TR/server-timing/) to response headers.

You can use this as a express module / basic http function.

# Install

```
$ npm install server-timing -S
```

# Usage

```javascript
const express = require('express')
const app = express()
app.use(serverTiming())

app.use((req, res, next) => {
  res.setMetric('db', 100.0, "Database metric");
  res.setMetric('api', 200.0, "HTTP/API metric");
  res.setMetric('cache', 300.0, "cache metric");
  next();
});
```

# Result
![image](https://cloud.githubusercontent.com/assets/555645/22737265/b5b5204e-ee45-11e6-82c5-776a5313d120.png)
