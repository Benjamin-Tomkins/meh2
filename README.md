# meh2

{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "type": "object",
  "properties": {
    "MakeItFail": {
      "type": "boolean"
    }
  },
  "required": ["MakeItFail"],
  "additionalProperties": false
}
```
plugins:
  - name: request-validator
    config:
      verbose_response: true
      body_schema:
        $schema: http://json-schema.org/draft-04/schema#
        type: object
        properties:
          MakeItFail:
            type: boolean
        required:
          - MakeItFail
        additionalProperties: false
```

```
plugins:
  - name: request-validator
    config:
      verbose_response: true
      body_schema: |
        {
          "$schema": "http://json-schema.org/draft-04/schema#",
          "type": "object",
          "properties": {
            "MakeItFail": {
              "type": "boolean"
            }
          },
          "required": ["MakeItFail"],
          "additionalProperties": false
        }

```
