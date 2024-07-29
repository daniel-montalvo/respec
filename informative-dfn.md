# `informative-dfn`

Enable this [lint rule](lint) to get a warning if an informative definition is used in a normative section.
    
You can fix your document by making the definition normative or use a local normative proxy for the definition like `<dfn data-cite="spec">term</dfn>`.

To silence this warning entirely, set `lint: { "informative-dfn": false }` in your `respecConfig`.

```js "example": "Enable informative-dfn linter rule."
var respecConfig = {
  lint: {
    "informative-dfn": true
  },
};
```
