---
sidebar_position: 1
---

# Text

The `Text` component is a flexible wrapper around standard HTML text elements such as `<p>`, `<span>`, or `<div>`. It allows you to apply consistent typography styles using Tailwind CSS classes, including font size, weight, color, and truncation.

## 📦 Import

```js
import { Text } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name        | Type                                  | Default             | Description |
|-------------|---------------------------------------|---------------------|-------------|
| `as`        | `elementType`                         | `"p"`               | The HTML element to render (e.g., `p`, `span`, `div`) |
| `size`      | One of: `"xs"`, `"sm"`, `"base"`, `"lg"`, `"xl"`, `"2xl"`, ..., `"9xl"` | `"base"`            | Tailwind text size class |
| `weight`    | One of: `"thin"`, `"extralight"`, `"light"`, `"normal"`, `"medium"`, `"semibold"`, `"bold"`, `"extrabold"`, `"black"` | `"normal"` | Font weight class |
| `color`     | `string`                              | `"text-gray-900"`   | Tailwind text color class |
| `truncate`  | `boolean`                             | `false`             | Whether to apply the `truncate` utility |
| `className` | `string`                              | `""`                | Additional Tailwind or custom class names |
| `children`  | `node` (required)                     | —                   | The text content to display |

## 🚀 Examples

### Basic Usage

```jsx
<Text>This is a base-sized, normal weight paragraph.</Text>
```

### Custom Size and Weight

```jsx
<Text size="xl" weight="bold">
  Bold and extra-large text
</Text>
```

### Truncation Example

```jsx
<Text truncate className="w-40">
  This is a long text that will be truncated.
</Text>
```

### Using a Custom Element

```jsx
<Text as="span" size="sm" color="text-blue-600">
  Blue span text
</Text>
```

## 💡 Best Practices

- Use semantic elements with the `as` prop (e.g., use `"label"` for form labels).
- Ensure a limited width on the container when using `truncate`.
- Stick to Tailwind's theme colors for consistency in design.
- Prefer `Text` over raw HTML elements when styling is required.