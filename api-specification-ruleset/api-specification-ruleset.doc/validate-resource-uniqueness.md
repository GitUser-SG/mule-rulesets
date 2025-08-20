
[Home](pages/home) > validate-resource-uniqueness

------

## Guidance
Resource identifiers must be unique within a single URL path to avoid ambiguity and confusion.


## Message
Path `{{apiContract.path}}` contains duplicate resource identifiers


## Examples
### valid
```yaml
openapi: "3.0.0"
  info:
    version: 1.0.0
    title: valid example
paths:
  /v1/users/{userId}/orders/{orderId}:
    get:

```
### invalid
```yaml
openapi: "3.0.0"
  info:
    version: 1.0.0
    title: invalid example
paths:
  /v1/users/{id}/users/{userId}:
    get:

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#EndPoint" target="_blank">EndPoint</a>

### Constraint


##### Type: Rego Validation 