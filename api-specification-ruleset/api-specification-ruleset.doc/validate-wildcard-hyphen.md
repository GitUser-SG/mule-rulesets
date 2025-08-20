
[Home](pages/home) > validate-wildcard-hyphen

------

## Guidance
When APIs need to read across multiple collections, use hyphen (-) as the wildcard character for consistency.


## Message
Path `{{apiContract.path}}` should use hyphen (-) as wildcard character instead of other symbols


## Examples
### valid
```yaml
openapi: "3.0.0"
  info:
    version: 1.0.0
    title: valid example
paths:
  /v1/users/-/orders:
    get:

```
### invalid
```yaml
openapi: "3.0.0"
  info:
    version: 1.0.0
    title: invalid example
paths:
  /v1/users/*/orders:
    get:
  /v1/users/all/orders:
    get:
  /v1/users/_/orders:
    get:

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#EndPoint" target="_blank">EndPoint</a>

### Constraint


##### Type: Declarative Validation 