
[Home](pages/home) > validate-query-param-snakecase

------

## Guidance
Multi-word query parameters and their values must use lower_snake_case convention for consistency.


## Message
Query parameter `{{apiContract.paramName}}` must use lower_snake_case


## Examples
### valid
```yaml
openapi: "3.0.0"
  info:
    version: 1.0.0
    title: valid example
parameters:
  - name: created_date
  - name: order_status
  - name: order
```

### invalid
```yaml
openapi: "3.0.0"
  info:
    version: 1.0.0
    title: invalid example
parameters:
  - name: createdDate
  - name: OrderStatus
  - name: Order-Id

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#Parameter" target="_blank">Parameter</a>

### Constraint


##### Type: Rego Validation 