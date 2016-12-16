# Intertron

A way to expose functions to your Electron renderer process, to be used with [Intertron Client](https://github.com/AragonOne/intertron-client)

`npm install intertron`

```javascript
const Intertron = require('intertron')

class DoSomething {
  static method(arg1, cb) {
    setTimeout(() => {
      cb(null, 'res')
    }, 100)
  }
}

new Intertron({ DoSomething })
```

And then the client will be able to call that method seamlessly as specified in [Intertron Client](https://github.com/AragonOne/intertron-client)
