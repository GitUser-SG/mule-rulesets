
[Home](pages/home) > validate-resource-verb-restriction

------

## Guidance
REST resources should represent entities (nouns), not actions (verbs). Use HTTP methods (GET, POST, PUT, DELETE) to represent actions. RPC operations using colon syntax (e.g., /users:activate) are exempt.


## Message
Resource identifier in path `{{apiContract.path}}` contains verbs. Resources MUST NOT  include verbs except when preceded by colon (:) for RPC operations


## Examples
### valid
```yaml
openapi: "3.0.0"
info:
  version: 1.0.0
  title: valid example
paths:
  /users:
  /orders:
  /products/{productId}:
  /users:activate:    # RPC operation - allowed
  /reports:generate:  # RPC operation - allowed

```
### invalid
```yaml
openapi: "3.0.0"
info:
  version: 1.0.0
  title: invalid example
paths:
  /getUsers:
  /createOrder:
  /updateUser:
  /deleteProduct:
  /searchResults:

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#EndPoint" target="_blank">EndPoint</a>

### Constraint


##### Type: Rego Validation 