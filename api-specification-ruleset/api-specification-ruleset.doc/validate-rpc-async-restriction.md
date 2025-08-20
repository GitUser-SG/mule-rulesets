
[Home](pages/home) > validate-rpc-async-restriction

------

## Guidance
RPC command names must not include `async` to maintain consistency in naming conventions.


## Message
RPC operation in path `{{apiContract.path}}` must not use `async` in command name


## Examples
### valid
```yaml
paths:
  /v1/users:activate:
    post:
      summary: Activate users
  /v1/orders:process:
    post:
      summary: Process orders

```
### invalid
```yaml
paths:
  /v1/users:activateAsync:
    post:
      summary: Invalid async naming
  /v1/orders:processAsync:
    post:
      summary: Invalid async naming

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#EndPoint" target="_blank">EndPoint</a>

### Constraint


##### Type: Declarative Validation 