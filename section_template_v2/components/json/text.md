# Render type `text` Properties only

| Property             | Type                  | Description                                                            | Default | Required | Example                                |
| -------------------- | --------------------- | ---------------------------------------------------------------------- | ------- | -------- | -------------------------------------- |
| `key`                | `string`              | Key of the JSON data to component value *`key` must be snake_case only |         | Yes      | `agent.first_name`                     |
| `label`              | `string`              | Label for component render                                             |         | No       |                                        |
| `renderType`         | `RenderType`          | For select component to render                                         | `text`  | No       |                                        |
| `valueType`          | `ValueType`           | Type of value to render                                                | `text`  | No       |                                        |
| `defaultValue`       | `any`                 | Default value to render                                                |         | No       |                                        |
| `textTemplate`       | `string`              | Text to render instead `key`                                           |         | No       | `${agent.firstName} ${agent.lastName}` |
| `showOnStatus`       | `string[]`            | Show component on status ...                                           |         | No       | `['draft', 'submit']`                  |
| `showOnProductTypes` | `string[]`            | Show component on product types ...                                    |         | No       | `['motor', 'health']`                  |
| `className`          | `string`              | Custom class name                                                      |         | No       | `text-primary`                         |
| `style`              | `React.CSSProperties` | Custom style                                                           |         | No       | `{ color: 'red' }`                     |

## Example

### Simple example `text`

```json
{
  "valueType": "number"
}
```

### Render from template

```json
{
  "textTemplate": "${agent.firstName} ${agent.lastName}",
}
```

### Need to render from status or product type condition

```json
{
  "valueType": "date",
  "showOnStatus": ["draft", "submit"],
  "showOnProductTypes": ["motor", "health"]
}
```

### Custom class name and style

```json
{
  "valueType": "price",
  "className": "text-primary",
  "style": {
    "backgroundColor": "red"
  }
}
```