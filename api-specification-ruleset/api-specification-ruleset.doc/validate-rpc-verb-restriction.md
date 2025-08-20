
[Home](pages/home) > validate-rpc-verb-restriction

------

## Guidance
RPC command names must not use standard REST method verbs to avoid confusion with standard REST operations.


## Message
RPC operation in path `{{apiContract.path}}` must not use standard REST verbs (get, list, create, update, delete)


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
  /v1/users:create:
    post:
      summary: Invalid RPC verb
  /v1/users:update:
    post:
      summary: Invalid RPC verb

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#EndPoint" target="_blank">EndPoint</a>

### Constraint


##### Type: Declarative Validation 