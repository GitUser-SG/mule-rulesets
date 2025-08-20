
[Home](pages/home) > validate-version-major-only

------

## Guidance
Version identifiers in API paths should only include major versions.


## Message
API endpoint `{{core.urlTemplate}}` must contain major version identifier (e.g., /v1/, not /v1.1/)


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
servers:
  - url: https://example.com/api/v1.1
  - url: https://example.com/api/version1.1

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#Server" target="_blank">Server</a>

### Constraint


##### Type: Declarative Validation 