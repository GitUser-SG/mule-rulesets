
[Home](pages/home) > validate-schema-preposition-restriction

------

## Guidance
Field names should be concise and avoid prepositions. Use direct relationships instead. For example, use 'userEmail' instead of 'emailOfUser'.


## Message
Field `{{shacl.name}}` contains prepositions.


## Examples
### valid
```yaml
components:
  schemas:
    User:
      properties:
        userEmail:
        orderDate:
        customerAddress:
        accountBalance:

```
### invalid
```yaml
components:
  schemas:
    User:
      properties:
        emailOfUser:
        dateForOrder:
        addressOfCustomer:
        balanceWithTax:
        priceFromVendor:

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#PropertyShape" target="_blank">PropertyShape</a>

### Constraint


##### Type: Rego Validation 