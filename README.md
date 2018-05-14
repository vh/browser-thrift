# browser-thrift

Patched version of Apache Thrift Node.js library to work either with Webpack /
Browserify or with nodejs.

### Usage

It is necessary to replace all `require('thrift')` with
`require('browser-thrift')` in the thrift generated files. You may use `sed`
for that:

```sh
for f in <gen_folder>/*; do
  sed -i '' -e \"s/'thrift'/'browser-thrift'/\" $f
done`
```
