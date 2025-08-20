
[Home](pages/home) > validate-server-endpoint

------

## Guidance
At least one server endpoint should be defined in the API specification


## Message
API specification must include server endpoint details


## Examples
### valid
```yaml
openapi: "3.0.0"
info:
  version: 1.0.0
  title: valid example
servers:
  - url: https://api.example.com/api/v1
    description: Production server
  - url: https://staging.example.com/api/v2
    description: Staging server

```
### invalid
```yaml
openapi: "3.0.0"
info:
  version: 1.0.0
  title: invalid example
paths: {}

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#WebAPI" target="_blank">WebAPI</a>

### Constraint


##### Type: Declarative Validation 