---
sidebar_position: 1
---

# Alert

A stylized alert box for displaying important messages to users. Supports icons, dismissibility, and multiple alert types like info, success, error, and warning.

## 📦 Import

```js
import { Alert } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name         | Type                                           | Default        | Description |
|--------------|------------------------------------------------|----------------|-------------|
| `message`    | `string` or `ReactNode`                        | — *(required)* | Message to display in the alert. |
| `type`       | `"info"` \| `"success"` \| `"error"` \| `"warning"` | `"info"`       | Type of alert, which determines the styling and default icon. |
| `onClose`    | `function`                                     | — *(required)* | Function to call when the alert is dismissed. |
| `className`  | `string`                                       | `""`           | Additional classes to apply to the container. |
| `dismissible`| `boolean`                                      | `true`         | Whether to show a close (`×`) button. |
| `icon`       | `string` (raw SVG) or `React.ElementType`      | —              | Optional custom icon. Falls back to the type's default if not provided. |
| `iconSize`   | `string`                                       | `"20px"`       | Width and height of the icon (e.g. `"24px"` or `"1.5rem"`). |

## 🎨 Styling

Each `type` value maps to specific background, text, and border colors using Tailwind CSS:

| Type     | Background    | Text           | Border        |
|----------|---------------|----------------|----------------|
| `info`   | `bg-blue-50`  | `text-blue-800`| `border-blue-200` |
| `success`| `bg-green-50` | `text-green-800`| `border-green-200` |
| `error`  | `bg-red-50`   | `text-red-800` | `border-red-200` |
| `warning`| `bg-yellow-50`| `text-yellow-800`| `border-yellow-200` |

## 🧪 Example

```jsx
<Alert
  message="Your profile was updated successfully!"
  type="success"
  onClose={() => console.log("Alert dismissed")}
/>
```

With custom icon:

```jsx
import { Info } from "lucide-react";

<Alert
  message="This is a custom info alert"
  type="info"
  icon={Info}
  onClose={() => console.log("Dismissed")}
/>
```

## 🧠 Notes

- Uses a `SvgIcon` utility component to render inline SVG strings for built-in icons.
- When `icon` is a string, it should be valid inline SVG markup.
- If `icon` is a React component (like an icon from `lucide-react`), it will be rendered using `React.createElement`.

## 💡 Use Cases

- Status updates (e.g., “Saved successfully”)
- Form error summaries
- System notifications
- Informational callouts
