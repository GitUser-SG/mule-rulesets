
[Home](pages/home) > validate-schema-verb-restriction

------

## Guidance
Schema names should represent domain entities, not operations or message wrappers. Use descriptive nouns that represent the business concept.


## Message
Schema `{{shacl.name}}` contains forbidden words incl. `Request`, `Response`, or verbs.


## Examples
### valid
```yaml
components:
  schemas:
    User:
    Order:
    Customer:

```
### invalid
```yaml
components:
  schemas:
    UserRequest:
    OrderResponse:
    CreateUser:
    UpdateOrder:

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#NodeShape" target="_blank">NodeShape</a>

### Constraint


##### Type: Rego Validation 