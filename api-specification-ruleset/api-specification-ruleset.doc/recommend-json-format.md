
[Home](pages/home) > recommend-json-format

------

## Guidance
While other media types are allowed, `application/json` is the recommended format for request and response bodies for better interoperability.


## Message
Consider using `application/json` as the preferred media type instead of `{{core.mediaType}}`


## Examples
### valid
```yaml
requestBody:
  content:
    application/json: {}
responses:
  '201':
    content:
      application/json: {}

```
### invalid
```yaml
requestBody:
  content:
    application/xml: {}
    text/plain: {}
```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#Payload" target="_blank">Payload</a>

### Constraint


##### Type: Declarative Validation 