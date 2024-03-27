# pico-server

A small experimental hackable HTTP server.

## Install

```
npm install pico-server
```

## Example

```
const { start_server } = require('../index.js');

start_server({
    host: 'localhost',
    port: 8000,
    public: './public'
    registry: {
        'demo': doDemo
    }
});

function doDemo(req,res) {
    res.writeHead(200);
    res.end('Hello World!');   
}
```

All files in the `public` directory will be served to the world. Directories and files can have a `.meta` JSON file which contains extra HTTP headers that should be added to the HTTP response.

