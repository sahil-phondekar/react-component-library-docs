---
sidebar_position: 2
---

# Icon Button
The `IconButton` component renders a button with only an icon. It's useful for icon-only interactions like toolbars, toggles, and quick actions. Fully accessible with required `aria-label` support and customizable via size, color, and disabled state.

## 📦 Import

```js
import { IconButton } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name        | Type                                                            | Default     | Description |
|-------------|-----------------------------------------------------------------|-------------|-------------|
| `icon`      | `string` (icon name) \| `React.ElementType` (icon component)    | — *(required)* | Icon to display |
| `className` | `string`                                                       | `""`        | Additional class names |
| `size`      | `"small"` \| `"medium"` \| `"large"`                            | `"medium"`  | Size of button and icon |
| `color`     | `string`                                                       | `"currentColor"` | Icon color |
| `disabled`  | `boolean`                                                      | `false`     | Disables the button |
| `onClick`   | `function`                                                     | —           | Click event handler |
| `ariaLabel` | `string`                                                       | — *(required)* | Descriptive label for screen readers |

## 📏 Sizes

| Size    | Padding  | Icon Size |
|---------|----------|-----------|
| `small` | `p-1.5`  | `16px`    |
| `medium`| `p-2`    | `20px`    |
| `large` | `p-3`    | `24px`    |

## 🎨 Customization

- **Icon**: Pass a string for a named icon (used with `SvgIcon`) or a custom React component.
- **Color**: Define any Tailwind-compatible color string, e.g. `text-red-500`, `#123456`, or keep default `currentColor`.

## 🚀 Examples

### With SVG icon name

```jsx
<IconButton icon="edit" ariaLabel="Edit item" onClick={() => alert("Edit")} />
```

### With custom React icon

```jsx
import { FaTrash } from "react-icons/fa";

<IconButton icon={FaTrash} ariaLabel="Delete item" onClick={handleDelete} />
```

### Disabled icon button

```jsx
<IconButton icon="lock" ariaLabel="Locked" disabled />
```

## 💡 Accessibility Tips

- `ariaLabel` is **required** to describe the action since there is no visible text.
- Use meaningful descriptions like `"Edit profile"`, `"Delete comment"`, or `"Open settings"`.
