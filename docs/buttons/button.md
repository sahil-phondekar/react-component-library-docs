---
sidebar_position: 1
---

# Button

The `Button` component provides a flexible and accessible way to create styled buttons with support for variants, sizes, icons, full-width layout, and custom colors. Built using Tailwind CSS and designed to be reused across your UI.

## 📦 Import

```js
import { Button } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name          | Type                                                                 | Default       | Description |
|---------------|----------------------------------------------------------------------|---------------|-------------|
| `variant`     | `"primary"` \| `"secondary"` \| `"transparent"` \| `"danger"` \| `string` | `"primary"` | Button style variant |
| `size`        | `"small"` \| `"medium"` \| `"large"`                                 | `"medium"`    | Size of the button |
| `icon`        | `string` (for SVG icon name) \| `elementType` (React component)      | —             | Optional icon (before label/children) |
| `label`       | `string`                                                             | —             | Optional label text (alternative to `children`) |
| `className`   | `string`                                                             | `""`          | Additional class names |
| `disabled`    | `bool`                                                               | `false`       | Disables the button |
| `fullWidth`   | `bool`                                                               | `false`       | Makes button span full width of its container |
| `customColors`| `object` `{ base, hover, focus, active }`                            | —             | Custom Tailwind classes to override default variant styles |
| `children`    | `node`                                                               | —             | Button content (text or JSX) |
| `onClick`     | `function`                                                           | —             | Click event handler |

## 🎨 Variants

| Variant     | Description                             |
|-------------|-----------------------------------------|
| `primary`   | Solid blue button with white text       |
| `secondary` | Light gray button with dark text        |
| `transparent` | Transparent with blue border and text |
| `danger`    | Red button for destructive actions      |

## 📏 Sizes

| Size    | Padding         | Font Size | Icon Size |
|---------|------------------|-----------|------------|
| `small` | `py-1.5 px-3`    | `text-sm` | `16px`     |
| `medium`| `py-2.5 px-5`    | `text-base` | `20px`   |
| `large` | `py-3 px-6`      | `text-lg` | `24px`     |

## 🚀 Examples

### Basic Usage

```jsx
<Button onClick={() => alert("Clicked!")}>Click Me</Button>
```

### With Icon and Label

```jsx
<Button icon="check" label="Confirm" variant="primary" />
```

### Custom Color Variant

```jsx
<Button
  customColors={{
    base: "bg-green-600 text-white",
    hover: "hover:bg-green-700",
    focus: "focus:ring-green-500",
    active: "active:bg-green-800",
  }}
>
  Success
</Button>
```

### Full Width Button

```jsx
<Button fullWidth>Submit</Button>
```

## 💡 Best Practices

- Use semantic actions and clear labeling for accessibility.
- Avoid placing too much content inside a button.
- Use `icon` along with a `label` or `children` for clear visual indicators.