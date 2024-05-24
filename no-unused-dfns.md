# `no-unused-dfns`

Enable this [lint rule](lint) to get a warning if an internal or un-exported definition is not used, i.e. there is nothing linking to that definition in given spec.

You can fix this by removing the `<dfn>` element or use another HTML element than `<dfn>` for that definition, or add `class="export"` to the definition.

To silence this warning entirely, set `lint: { "no-unused-dfns": false }` in your `respecConfig`.


```js "example": "Enable no-unused-dfns linter rule."
var respecConfig = {
  lint: {
    "no-unused-dfns": true,
  },
};
```
