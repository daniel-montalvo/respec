# `informative-dfn`

Enable this [lint rule](lint) to get a warning if an informative definition is used in a normative section.
    
You can fix your document by making the definition normative, or add a `class="lint-ignore"` attribute to the link
or use a local normative proxy for the definition like `<dfn data-cite="spec">term</dfn>`.

To silence this warning entirely, set `lint: { "no-unused-dfns": false }` in your `respecConfig`

```js "example": "Disable informative-dfns linter rule."
var respecConfig = {
  lint: {
    "no-unused-dfns": false,
  },
};
```
