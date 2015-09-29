---
layout: splash.html
---

__Example: a bare bones microservice__
```javascript
var seneca = require('seneca')()

seneca.add({ role:'user', cmd:'login' }, function (args, callback) {
  callback(null, { loggedIn:true })
})

seneca.listen()
```

__Example: a bare bones client__
```javascript
var seneca = require('seneca')()
var client = seneca.client()

client.act({ role:'user', cmd:'login' }, function (err, result) {
  console.log(result.loggedIn)
})
```
