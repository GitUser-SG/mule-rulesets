
[Home](pages/home) > validate-resource-alternation

------

## Guidance
API paths should follow the pattern of alternating between resource identifiers and parameter values for clear hierarchical structure.


## Message
Path `{{apiContract.path}}` contains consecutive parameters which must be avoided


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
  /v1/users/orders/{userId}/{orderId}:
    get:

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#EndPoint" target="_blank">EndPoint</a>

### Constraint


##### Type: Rego Validation 