---
sidebar_position: 4
---

# Tooltip

A lightweight and customizable tooltip component that displays a message when the user hovers, focuses, or taps on an element.

## 📦 Import

```js
import { Tooltip } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name            | Type                                   | Default   | Description |
|-----------------|----------------------------------------|-----------|-------------|
| `children`      | `ReactElement`                         | — *(required)* | The element that triggers the tooltip on hover/focus. Must be a single React element. |
| `text`          | `string | ReactNode`                   | — *(required)* | The content of the tooltip. Can be a string or any valid React node. |
| `position`      | `"top" | "bottom" | "left" | "right"` | `"top"`    | Tooltip position relative to the child element. |
| `className`     | `string`                               | `""`       | Additional class for the outer wrapper. |
| `tooltipClass`  | `string`                               | `""`       | Additional class for the tooltip itself. |
| `delay`         | `number`                               | `200`      | Delay in milliseconds before showing/hiding the tooltip. |
| `disabled`      | `boolean`                              | `false`    | If `true`, disables tooltip behavior entirely. |
| `arrowSize`     | `string`                               | `"5px"`    | Controls the size of the tooltip arrow. Should be a valid CSS unit (e.g., `5px`, `0.5rem`). |

## 🎨 Styling

- **Tooltip container**: Uses Tailwind classes for layout and appearance (`bg-gray-800 text-white text-sm px-3 py-2 rounded shadow-lg`).
- **Arrow**: A small CSS triangle using border styles, with customizable size using the `arrowSize` prop.
- **Positioning**: Supports top, bottom, left, and right placement using absolute positioning and transform utilities.

## 🧪 Example

```jsx
<Tooltip text="This is a tooltip" position="right">
  <button className="btn">Hover me</button>
</Tooltip>
```

You can also use custom content inside the tooltip:

```jsx
<Tooltip text={<span><strong>Tip:</strong> Click here to proceed</span>}>
  <span className="underline cursor-pointer">Hover text</span>
</Tooltip>
```

## 🧠 Accessibility Notes

- The child element gets a `tabIndex` to support keyboard navigation.
- Tooltip opens on `focus` (keyboard) and `hover` (mouse), and closes on `blur` and `mouseleave`.

## 🧩 Tooltip Arrow Customization

The arrow is created with pure CSS. The arrow color is tied to the tooltip background (`gray-800`). If you customize the background, make sure to adjust the arrow border color in the CSS utility classes or via the `tooltipClass`.
