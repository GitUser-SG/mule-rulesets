
[Home](pages/home) > validate-schema-error-model

------

## Guidance
All schemas used in HTTP 4xx and 5xx error responses must implement the standardized error response model containing the following required fields: - apiVersion: String indicating the API version - errorCode: String with a specific error code identifier - errorMessage: String with human-readable error description - errorStatus: Integer with HTTP status code - errorDetails: Object with additional error information (optional)


## Message
Schemas used in error responses must include required error fields: apiVersion, errorCode, errorMessage, errorStatus


## Examples
### valid
```yaml
paths:
  /v1/users:
    get:
      responses:
        '400':
          description: Bad Request
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/ErrorResponse'
components:
  schemas:
    ErrorResponse:
      type: object
      required:
        - apiVersion
        - errorCode
        - errorMessage
        - errorStatus

```
### invalid
```yaml
paths:
  /v1/users:
    get:
      responses:
        '400':
          description: Bad Request
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/BadErrorResponse'

components:
  schemas:
    BadErrorResponse:
      type: object
      properties:
        message:
          type: string

```

> Applies to <a href="https://github.com/aml-org/amf/blob/develop/documentation/model.md#WebAPI" target="_blank">WebAPI</a>

### Constraint


##### Type: Rego Validation 