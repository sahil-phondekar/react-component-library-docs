---
sidebar_position: 2
---

# Card

A versatile container component that wraps content with padding, shadow, and optional hover effects. Great for grouping related information like dashboards, panels, or content sections.

## 📦 Import

```js
import { Card } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name         | Type                                         | Default    | Description |
|--------------|----------------------------------------------|------------|-------------|
| `children`   | `ReactNode`                                  | **Required** | The content to be rendered inside the card. |
| `className`  | `string`                                     | `""`         | Additional Tailwind or custom class names. |
| `rounded`    | `"none" \| "sm" \| "md" \| "lg" \| "xl" \| "2xl" \| "3xl"` | `"md"` | Border radius of the card. |
| `hover`      | `boolean`                                    | `false`      | If `true`, applies hover elevation and subtle lift animation. |

## ✨ Features

- Pre-styled with white background and subtle shadow
- Customizable border radius via `rounded` prop
- Optional hover effect for better interactivity
- Composable and easily extendable via `className`

## 🧪 Examples

### Default Card

```jsx
<Card>
  <h3 className="text-lg font-semibold">Title</h3>
  <p>This is a simple card without hover effect.</p>
</Card>
```

### Hoverable Card with Rounded Corners

```jsx
<Card hover rounded="lg" className="p-6">
  <h3 className="text-xl font-bold">Dashboard</h3>
  <p className="text-gray-600">Hover to see the lift and shadow effect.</p>
</Card>
```

## 🧠 Notes

- The `hover` prop adds visual feedback when the card is hovered (shadow increase + slight translate).
- Combine with padding utility classes (`p-4`, `p-6`) for spacing control.
- Can be nested inside grids or flex layouts for responsive designs.
