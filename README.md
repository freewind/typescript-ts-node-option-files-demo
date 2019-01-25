TypeScript "ts-node" Option "files" Demo
=============================================

ts-node在默认情况下不会读取`tsconfig.json`中`files`中指定的文件，
而是根据指定要运行的ts文件的`import`s寻找。

在大多数情况下，这种做法是没有问题的，
但是有时候，比如定义了`.d.ts`文件并且没有使用`rootTypes`的方式，而是使用`files`中
引用的方式，则会出现`tsc`正常编译但是ts-node缺少类型的问题。

这种情况下，我们可以通过`rootTypes`的方式解决（在另一个demo中），
也可以使用`ts-node`新提供的`--files`要求ts-node载入相应的文件。

在某些情况下，也可以使用环境变量`TS_NODE_FILES`来指定值。

`files`的值应该是一个boolean，但是在使用时，需要注意：

- `--files`可以传入任何字符串，如果等于`false`则为`false`，其它值为`true`
- `TS_NODE_FILES`传入`true`则为`true`，其它值为`false`


```
npm install
npm run ts-node
npm run ts-node-env
```

Reference
---------

- https://github.com/TypeStrong/ts-node#help-my-types-are-missing
- https://www.typescriptlang.org/docs/handbook/tsconfig-json.html#types-typeroots-and-types
