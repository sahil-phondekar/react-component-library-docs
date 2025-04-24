---
sidebar_position: 3
---

# Divider

The `Divider` component visually separates content. It supports both horizontal and vertical orientations and can include optional text centered within the line. Built using Tailwind CSS classes, it's highly customizable in color and thickness.

## 📦 Import

```js
import { Divider } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name         | Type                                      | Default           | Description |
|--------------|-------------------------------------------|-------------------|-------------|
| `orientation`| `"horizontal"` \| `"vertical"`            | `"horizontal"`    | Direction of the divider line |
| `color`      | `string`                                  | `"border-gray-200"` | Tailwind border color class |
| `thickness`  | `string`                                  | `"border"`        | Tailwind border thickness (e.g., `border-2`) |
| `className`  | `string`                                  | `""`              | Additional custom class names |
| `children`   | `node`                                    | `null`            | Optional content (e.g., label) to show centered in the divider |

## 🚀 Examples

### Basic Horizontal Divider

```jsx
<Divider />
```

### Horizontal Divider with Label

```jsx
<Divider>OR</Divider>
```

### Vertical Divider

```jsx
<div className="flex h-20">
  <div>Left</div>
  <Divider orientation="vertical" />
  <div>Right</div>
</div>
```

### Custom Color and Thickness

```jsx
<Divider color="border-blue-500" thickness="border-2" />
```

## 💡 Best Practices

- Use a `Divider` to group related content or provide separation in layouts.
- Use the `children` prop for simple inline labels like `"OR"` or `"Step 1"`.
- For vertical dividers, place them between flex row items and set a height.