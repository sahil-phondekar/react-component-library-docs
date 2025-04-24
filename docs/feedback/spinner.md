---
sidebar_position: 4
---

# Spinner

A simple animated loading spinner using Tailwind CSS. Ideal for indicating ongoing background processes like data fetching or form submission.

## 📦 Import

```js
import { Spinner } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name       | Type     | Default         | Description |
|------------|----------|-----------------|-------------|
| `size`     | `string` | `"w-8 h-8"`      | Tailwind width and height classes. Controls the overall size. |
| `color`    | `string` | `"border-blue-500"` | Tailwind border color class. Applies to the top border to create the spinner illusion. |
| `className`| `string` | `""`            | Additional Tailwind classes for custom styling. |

## ✨ Features

- Uses `animate-spin` from Tailwind CSS for smooth rotation.
- Circular shape created using `border-t-2` and `rounded-full`.
- Accessible with `role="status"` and `aria-label="Loading"` for screen readers.
- Fully customizable with Tailwind utility classes.

## 🧪 Example

### Default Spinner

```jsx
<Spinner />
```

### Small White Spinner

```jsx
<Spinner size="w-4 h-4" color="border-white" />
```

### Large Custom Color Spinner

```jsx
<Spinner size="w-12 h-12" color="border-emerald-600" />
```

## 🧠 Notes

- Use it alongside a `Skeleton` or `Toast` to enrich loading states.
- Pair with absolute positioning and a backdrop for a global loading indicator.