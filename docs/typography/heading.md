---
sidebar_position: 2
---

# Heading

The `Heading` component renders styled heading elements (`h1` through `h6`, or custom tags) with consistent font sizes, weights, and colors using Tailwind CSS utilities. Ideal for maintaining a unified typographic hierarchy in your design system.

## 📦 Import

```js
import { Heading } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name        | Type                                  | Default             | Description |
|-------------|---------------------------------------|---------------------|-------------|
| `as`        | `elementType`                         | `"h1"`              | The HTML heading tag or element to render (`h1`, `h2`, ..., `div`) |
| `size`      | One of: `"xs"`, `"sm"`, `"base"`, `"lg"`, `"xl"`, `"2xl"`, ..., `"9xl"` | `"2xl"`            | Sets the heading size using Tailwind |
| `weight`    | One of: `"thin"`, `"extralight"`, `"light"`, `"normal"`, `"medium"`, `"semibold"`, `"bold"`, `"extrabold"`, `"black"` | `"bold"` | Font weight class |
| `color`     | `string`                              | `"text-gray-900"`   | Tailwind text color class |
| `className` | `string`                              | `""`                | Additional custom class names |
| `children`  | `node` (required)                     | —                   | Content to display inside the heading |

## 🚀 Examples

### Basic Usage

```jsx
<Heading>Welcome to the Dashboard</Heading>
```

### Custom Size and Tag

```jsx
<Heading as="h2" size="3xl">
  Section Title
</Heading>
```

### Custom Color and Weight

```jsx
<Heading color="text-blue-600" weight="semibold">
  Highlighted Heading
</Heading>
```

## 💡 Best Practices

- Use semantic HTML elements (`h1` to `h6`) with the `as` prop for SEO and accessibility.
- Stick to your design system's predefined size and weight scales for consistency.
- Use `Heading` only for actual titles or section headings—not for general text.