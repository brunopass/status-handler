# Status Parser

Node.js HTTP friendly responses handler

## Getting Started 🚀

### Instalation
_copy and paste this code into the terminal_
```
...
```

### Examples

_send response on success_
```
const router = require('express').Router()
const status = require('status-parser')

router.get('/', (req,res)=>{

    status.success(res).OK()

})
```

_add personalizated data response_
```
const router = require('express').Router()
const status = require('status-parser')

router.get('/', (req,res)=>{

    const data = {
        "friends": {}
    }

    status.success(res).OK(data)

})
```

_add personalizated headers_
```
const router = require('express').Router()
const status = require('status-parser')

router.get('/', (req,res)=>{

    const data = {
        "friends": {}
    }

    const options = {
        header: {
            "Content-Type": "application/json"
        }
    }

    status.success(res,options).OK(data)

})
```

_add personalizated cookie_
```
const router = require('express').Router()
const status = require('status-parser')

router.get('/', (req,res)=>{

    const data = {
        "friends": {}
    }

    const options = {
        header: {
            "Content-Type": "application/json"
        },
        cookie: {
            "name": "token",
            "val": "secret",
            options:{
                "httpOnly":true
            }
        }
    }

    status.success(res,options).OK(data)

})
```

## Author ✒️

* **Bruno Passarelli** - [brunopass](https://github.com/brunopass)

## Licence 📄

this project is licensed under the MIT license