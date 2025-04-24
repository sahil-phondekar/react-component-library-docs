---
sidebar_position: 1
---

# SvgIcon

A versatile icon component that renders SVG icons either as inline SVGs or by rendering the provided SVG markup. This component allows you to customize the size, color, and viewbox, and can handle both SVG paths and full SVG markup.

## 📦 Import

```js
import { SvgIcon } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name           | Type         | Default       | Description                                                                 |
|----------------|--------------|---------------|-----------------------------------------------------------------------------|
| `svg`          | `string`     | **Required**  | The SVG path or full SVG markup to render.                                   |
| `className`    | `string`     | `""`          | Additional custom class names for styling the SVG icon.                      |
| `size`         | `string`     | `"24px"`      | The size of the icon, can be specified in any valid CSS unit (e.g., `px`, `rem`). |
| `color`        | `string`     | `"currentColor"` | The color of the icon, defaults to `currentColor` to inherit from the parent. |
| `viewBox`      | `string`     | `"0 0 24 24"` | The viewBox attribute for the SVG element.                                   |

## ✨ Features

- **Supports Path & Full SVG Markup:** Can render both SVG paths and full SVG markup.
- **Customizable Size & Color:** Customize the size and color using `size` and `color` props.
- **SVG Rendering:** Optimized for rendering SVGs efficiently within a React component.

## 🧪 Example Usage

### Basic Usage with Path

```jsx
<SvgIcon svg="M12 2L2 12h4v8h8v-8h4z" size="40px" color="blue" />
```

### With Full SVG Markup

```jsx
<SvgIcon svg="<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'><path d='M12 2L2 12h4v8h8v-8h4z'/></svg>" size="48px" color="green" />
```

## 🧠 Notes

- **Path vs Full SVG:** The component detects if the `svg` prop is a path or a full SVG markup based on whether the string starts with `<svg`.
- **Dangerous HTML:** The component uses `dangerouslySetInnerHTML` to inject full SVG markup. Ensure that the SVG markup you pass is sanitized and safe.
- **Responsive Size:** You can use any valid CSS unit (e.g., `px`, `em`, `rem`, `%`) to control the size of the icon.
