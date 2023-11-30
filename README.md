# meh2

```
plugins:
  - name: post-function
    config:
      functions:
        - |
          local function replace_message_with_errors(body)
            return string.gsub(body, "message", "errors")
          end

          local response_status = kong.response.get_status()
          if response_status == 400 then
            local body = kong.service.response.get_body()
            if type(body) == "string" then
              local new_body = replace_message_with_errors(body)
              kong.service.response.set_raw_body(new_body)
            end
          end
```

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
