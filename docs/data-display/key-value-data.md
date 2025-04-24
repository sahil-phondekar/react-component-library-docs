---
sidebar_position: 5
---

# KeyValueData

A flexible, responsive component to display key-value pairs in a grid layout. Useful for showing structured metadata or object details in dashboards or information panels.

## 📦 Import

```js
import { KeyValueData } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                   | Type      | Default                          | Description |
|------------------------|-----------|----------------------------------|-------------|
| `data`                 | `object`  | — *(required)*                   | An object with key-value pairs to display. |
| `title`                | `string`  | `undefined`                      | Optional title to display above the key-value data. |
| `className`            | `string`  | `""`                             | Custom class for the outer container. |
| `gridStyle`            | `string`  | `"sm:grid-cols-1 md:grid-cols-3"`| Tailwind classes to control the responsive grid layout. |
| `keyValueContainerStyle` | `string` | `""`                            | Additional class for each key-value container block. |
| `keyStyle`             | `string`  | `"text-sm font-medium text-gray-600"` | Tailwind classes for styling keys. |
| `valueStyle`           | `string`  | `"text-sm text-gray-900 break-all"`  | Tailwind classes for styling values. |
| `titleStyle`           | `string`  | `"text-lg font-semibold mb-4"`  | Tailwind classes for styling the optional title. |

## 🎨 Styling

- The layout uses Tailwind’s responsive grid utilities via the `gridStyle` prop.
- Each key and value is styled independently with `keyStyle` and `valueStyle`.
- The overall component has padding, background color, and rounded corners by default.

## 🧪 Example

```jsx
<KeyValueData
  title="User Info"
  data={{
    Name: "John Doe",
    Email: "john@example.com",
    Role: "Administrator",
    Active: true,
  }}
  gridStyle="sm:grid-cols-1 md:grid-cols-2"
  className="my-4"
/>
```

## ❓ Edge Case Handling

- If `data` is `null`, `undefined`, or an empty object, the component renders nothing (`null`).
- If a value is `null` or `undefined`, a dash `"-"` is displayed in its place.
- All values are converted to strings for display.

## 💡 Use Cases

- Displaying detailed object metadata
- Admin dashboards
- User profile information
- API response previews