TypeScript "ts-node" Use *.d.ts Files Demo
==========================================

Note: the parameter `ts-node` provided is not just the same as `node` and `tsc`,
sometimes, `tsc` works well, but `ts-node` doesn't.

To use `*.d.ts` along with our code, we need to use the new `--files` provided
in `ts-node` to specify the `*.d.ts` files to make project compilable.

```
npm install
npm run tsc
npm run ts-node
```

