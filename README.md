# tinyify-global-url-bug

a reproducible test case for a bug somewhere in `tinyify`

```shell
git clone git://github.com/ahdinosaur/tinyify-global-url-bug
cd tinyify-global-url-bug
npm install
npm test
```

notice that the final expression in `index.js`

```js
new URL('test')
```

is now

```
new ie('test')
```

where `ie` is the same mangled name as the `URL` variable from within the `ajv/lib/compile/formats.js` module.
