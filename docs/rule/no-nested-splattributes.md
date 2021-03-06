# no-nested-splattributes

Having `...attributes` on multiple elements nested within each other in a
component can cause unintended results.

This rule prevent you from running into this issue by disallowing
`...attributes` if any of the parent elements already has `...attributes` on it.

## Examples

This rule **forbids** the following:

```hbs
<div ...attributes>
  <div ...attributes>
    ...
  </div>
</div>
```

This rule **allows** the following:

```hbs
<div ...attributes>...</div>
<div ...attributes>...</div>
```

## Migration

- Remove the inner `...attributes` declaration
