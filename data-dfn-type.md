# `data-dfn-type`

You can add a `data-dfn-type` attribute on `<dfn>` elements to declare the type of definition. This is used in conjunction with [`data-link-type`](data-link-type) to allow linking to a definition of particular type.

to properly scope a definition, It's recommended that you add an accepted `data-dfn-type` value. Accepted values include:

CSS:

* property
* descriptor (the things inside at-rules like @font-face)
* value (any value that goes inside of a property, at-rule, etc.)
* type (an abstract type for CSS grammars, like <length> or <image>)
* at-rule
* function (like counter() or linear-gradient())
* selector

WebIDL:

* interface
* constructor
* method
* argument
* attribute
* callback
* dictionary
* dict-member
* enum
* enum-value
* exception (for new DOMException names)
* const
* typedef
* stringifier
* serializer
* iterator
* maplike
* setlike
* extended-attribute (things like [EnforceRange])

HTML/SVG/etc element definitions:

* element
* element-state (a spec concept, like <input> being in the "password state")
* element-attr
* attr-value

CDDL:

* cddl-module (when spec needs to define multiple CDDL modules)
* cddl-type (things like actual types and groups)
* cddl-key (member names in type or group definitions)
* cddl-value (values in an enumeration)
* cddl-parameter (generic parameter names)

URL schemes:

* scheme

HTTP headers:

* http-header

Grammar operators:

* grammar

Browser permissions:

* permission
"English" terms:

* abstract-op (for "English-language algorithms")
* dfn (for general terms and phrases, and a catch-all for anything else)

```html "example": "Specifying data-dfn-type."
<p>
  The document has visibility state of
  <dfn id="dfn-hidden" data-dfn-type="dfn">hidden</dfn>.
</p>
<p>
  `visibilityState` attribute has value
  <dfn id="idl-hidden" data-dfn-type="idl">hidden</dfn>.
</p>

<p>
  {{ hidden }} links to dfn with id="idl-hidden". This is same
  <a data-link-type="idl">hidden</a>, but above syntax is preferred.
</p>
<p>
  [= hidden =] links to dfn with id="dfn-hidden". This is same
  <a data-link-type="dfn">hidden</a>, but above syntax is preferred.
</p>
```
