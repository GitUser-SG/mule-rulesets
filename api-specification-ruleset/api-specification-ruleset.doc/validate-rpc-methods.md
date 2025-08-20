
[Home](pages/home) > validate-rpc-methods

------

## Guidance
RPC operations (identified by colon syntax) are only allowed with GET or POST HTTP methods to maintain consistency.


## Message
RPC operation with method `{{apiContract.method}}` MUST only use GET or POST methods.


## Examples
### valid
```yaml
paths:
  /v1/users:activate:
    post:
      summary: Activate users
  /v1/reports:generate:
    get:
      summary: Generate reports

```
### invalid
```yaml
paths:
  /v1/users:activate:
    put:
      summary: Invalid method for RPC
  /v1/users:deactivate:
    delete:
      summary: Invalid method for RPC

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#Operation" target="_blank">Operation</a>

### Constraint


##### Type: Rego Validation 