# Webpack - The Good Parts

* [Slides](https://presentations.survivejs.com/webpack-the-good-parts/)
* [Book](https://survivejs.com/webpack/)

## Goals

* Understand the basic concepts of webpack.
* Understand the capabilities of webpack.

## Examples

**Loader**

```javascript
module.exports = (input) => input + input;
```

**Resolve**

```javascript
import foo from 'foo'; // resolve node_modules/

...
```

```javascript
const config = {
  resolve: {
    alias: {
      foo: path.join(__dirname, 'foo.js')
    },
    extensions: [
      '.jsx'
    ],
    modules: [
      path.join(__dirname, 'my_modules'),
      'node_modules'
    ],
  },
}
```

**Loader order**

```javascript
const config = {
  test: /\.css$/,
  use: ['style-loader', 'css-loader'],
}
```

```javascript
styleLoader(cssLoader(input))
```
