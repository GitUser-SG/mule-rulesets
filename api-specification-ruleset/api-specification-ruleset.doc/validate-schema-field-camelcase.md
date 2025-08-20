
[Home](pages/home) > validate-schema-field-camelcase

------

## Guidance
Request and response body field names must use camelCase convention for consistency across API specifications.


## Message
Field name `{{shacl.name}}` should use camelCase


## Examples
### valid
```yaml
components:
  schemas:
    User:
      type: object
      properties:
        firstName:
          type: string
        lastName:
          type: string
        emailAddress:
          type: string

```
### invalid
```yaml
components:
  schemas:
    User:
      type: object
      properties:
        first_name:
          type: string
        LastName:
          type: string
        email-address:
          type: string

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#PropertyShape" target="_blank">PropertyShape</a>

### Constraint


##### Type: Declarative Validation 