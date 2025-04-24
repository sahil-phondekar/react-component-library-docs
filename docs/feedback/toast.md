---
sidebar_position: 2
---

# Toast

A lightweight toast notification component that shows transient messages. Supports various types, automatic dismissal, positioning, and custom icons.

## 📦 Import

```js
import { Toast } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name         | Type                                           | Default         | Description |
|--------------|------------------------------------------------|------------------|-------------|
| `message`    | `string` or `ReactNode`                        | — *(required)*  | Content to display inside the toast. |
| `type`       | `"info"` \| `"success"` \| `"error"` \| `"warning"` | `"info"`      | The style of the toast. Sets color and default icon. |
| `isOpen`     | `boolean`                                      | — *(required)*  | Controls the visibility of the toast. |
| `onClose`    | `function`                                     | — *(required)*  | Callback triggered when the toast is closed (auto or manual). |
| `duration`   | `number`                                       | `3000`          | Duration in ms before the toast auto-dismisses. Use `0` to disable auto-close. |
| `icon`       | `string` (raw SVG) or `React.ElementType`      | —               | Custom icon to override the default one based on `type`. |
| `position`   | `"top-left"` \| `"top-right"` \| `"bottom-left"` \| `"bottom-right"` | `"bottom-right"` | Controls where the toast appears on screen. |
| `className`  | `string`                                       | `""`            | Additional Tailwind CSS classes for custom styling. |

## 📍 Positioning

| Value           | Description                |
|-----------------|----------------------------|
| `top-left`      | Top-left corner of viewport |
| `top-right`     | Top-right corner            |
| `bottom-left`   | Bottom-left corner          |
| `bottom-right`  | Bottom-right corner         |

## 🎨 Type Styling

| Type     | Background     | Default Icon                           |
|----------|----------------|----------------------------------------|
| `info`   | `bg-blue-500`  | Info circle                            |
| `success`| `bg-green-500` | Checkmark                              |
| `error`  | `bg-red-500`   | Cross (X)                              |
| `warning`| `bg-yellow-500`| Warning exclamation                    |

## 🧪 Example

```jsx
<Toast
  message="This is an info toast!"
  type="info"
  isOpen={isOpen}
  onClose={() => setIsOpen(false)}
  duration={4000}
/>
```

With custom position and icon:

```jsx
import { AlertTriangle } from "lucide-react";

<Toast
  message="Be cautious of the changes"
  type="warning"
  icon={AlertTriangle}
  position="top-right"
  isOpen={toastVisible}
  onClose={() => setToastVisible(false)}
/>
```

## 🧠 Notes

- The toast will auto-dismiss based on the `duration` prop.
- If `duration` is `0`, it must be dismissed manually using the close button.
- Uses a `SvgIcon` helper component to handle inline SVG string rendering.
- When `icon` is a React component (e.g., from `lucide-react`), it's rendered via `React.createElement`.

## 💡 Use Cases

- Form submission success/failure
- System warnings or messages
- Timed alerts or user feedback