
[Home](pages/home) > validate-resource-camelcase

------

## Guidance
Multi-word resource identifiers must use camelCase convention.


## Message
Resource identifier in path `{{apiContract.path}}` should use camelCase for multi-word resources


## Examples
### valid
```yaml
openapi: "3.0.0"
info:
  version: 1.0.0
  title: valid example
paths:
  /{applicationId}/auth/entitlements:
    get:
  /orderItems:
    get:
  /api/-/users:
    get:

```
### invalid
```yaml
openapi: "3.0.0"
info:
  version: 1.0.0
  title: invalid example
paths:
  /{applicationId}/order-items:
    get:
  /user_profiles:
    get:

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#EndPoint" target="_blank">EndPoint</a>

### Constraint


##### Type: Declarative Validation 