A simple and configurable mock server with UI console for websocket, with which you can either send message manually or make rules to get matched response. Err... It's hard to summarize, Let's take a look!

# Installation

```
npm install websocket-mock-server
```

or

```
yarn add websocket-mock-server
```

# Configuration

package.json
```json
{
  "script": {
    "wsmock": "wsmock -c CONFIG_PATH"
  }
}
```

The following config.js will be used and watched as default config when no `CONFIG_PATH` is provided.
```javascript
module.exports = {
  port: 4040,
  // a function exported to handle specific input and return output which will be sending later.
  rule: function (input) {}
  // set the delay time before sending auto message 
  autoMsgTimeout: 1000,
};
```

# UI Console

UI Console provide a chatroom-like way for you to send WebSocket message to server, which will be broadcast to other clients.

![preview](./public/img/preview.png)