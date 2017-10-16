```
npm init -y
```

```
npm install express --save
```

New file called app.js at the route:

```
const express = require('express')
const app = express()

app.get('/', function (req, res) {
  res.send('Hello World!')
})

app.listen(3000, function () {
  console.log('Example app listening on port 3000!')
})
```

Add a html file and change the express set up so that it renders the HTML file:

```
const express = require('express');
const app = express();
var path = require("path");

app.get('/', function (req, res) {
  res.sendFile(path.join(__dirname+'/index.html'));
});

app.listen(3000, function () {
  console.log('Example app listening on port 3000!');
});
```
