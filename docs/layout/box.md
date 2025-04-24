---
sidebar_position: 1
---

# Box

The `Box` component is a simple, flexible wrapper that lets you render any HTML element or custom component using the `as` prop. It’s great for building composable layouts.

## 📦 Import

```js
import { Box } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name         | Type                    | Default     | Description |
|--------------|-------------------------|-------------|-------------|
| `children`   | `ReactNode`             | **Required**| Content inside the box. |
| `className`  | `string`                | `""`        | Tailwind or custom classes for styling. |
| `as`         | `elementType`           | `"div"`     | The HTML tag or React component to render. |

---

## ✨ Features

- Renders any valid HTML tag (`div`, `section`, `article`, etc.) or custom component
- Passes all other props to the rendered element
- Useful for layout abstraction and consistent box styling

## 🧪 Example

### Render as a `section`

```jsx
<Box as="section" className="p-4 bg-gray-100 rounded">
  <h2 className="text-lg font-bold">Section Title</h2>
  <p>This is a section using the Box component.</p>
</Box>
```

### Render as a `button`

```jsx
<Box
  as="button"
  type="button"
  className="px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700"
  onClick={() => alert("Clicked!")}
>
  Click Me
</Box>
```

## 🧠 Notes

- `as` is especially useful when creating styled wrappers that adapt to semantic HTML needs.
- Always ensure to pass necessary accessibility props when rendering interactive elements (e.g., `role`, `aria-*`, `tabIndex`).
