
[Home](pages/home) > validate-rpc-preposition-restriction

------

## Guidance
RPC commands should use simple verbs without prepositions. Keep command names concise and action-focused.


## Message
RPC command `{{apiContract.path}}` contains prepositions.


## Examples
### valid
```yaml
paths:
  /users:activate:
  /orders:process:
  /reports:generate:
  /accounts:suspend:
  /notifications:send:

```
### invalid
```yaml
paths:
  /users:activateFor:     # Contains preposition 'for'
  /orders:processWit:     # Contains preposition 'with'
  /reports:generateFor:   # Contains preposition 'for'
  /accounts:suspendBy:    # Contains preposition 'by'
  /data:exportTo:         # Contains preposition 'to'

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#EndPoint" target="_blank">EndPoint</a>

### Constraint


##### Type: Rego Validation 