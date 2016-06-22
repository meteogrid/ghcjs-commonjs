# ghcjs-commonjs-pandoc
GHCJS CommonJS pandoc example.

## Building
Running:
```
npm install
```

Will install dependencies. To build you can run:
```
npm run build
```

## Running
The generated code should be executable in **Node.js** and the **Browser**, but
only the **Node.js** build has been tested. Usage is:

- Compile with `stack build`

```javascript
const ghcjsRequire = require('ghcjs-require');
const Main = ghcjsRequire(module, 'ghcjs-commonjs-pandoc');
Main(({ wrapped }) => {
  wrapped.convert('markdown', 'html', '# Hello World')
    .then((res) => console.log(res));
});
```