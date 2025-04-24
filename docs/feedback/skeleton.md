---
sidebar_position: 3
---

# Skeleton

A lightweight utility component for creating animated loading placeholders. Perfect for showing content loading states in lists, cards, text, avatars, etc.

## 📦 Import

```js
import { Skeleton } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name           | Type     | Default       | Description |
|----------------|----------|---------------|-------------|
| `width`        | `string` | `"w-full"`    | Tailwind width utility (e.g., `w-32`, `w-1/2`). Controls the placeholder’s width. |
| `height`       | `string` | `"h-6"`       | Tailwind height utility (e.g., `h-4`, `h-10`). Controls the placeholder’s height. |
| `borderRadius` | `string` | `"rounded-md"`| Tailwind border radius utility (e.g., `rounded`, `rounded-full`). |
| `className`    | `string` | `""`          | Additional Tailwind CSS classes for custom styles. |

## ✨ Features

- `animate-pulse` animation simulates a pulsing effect to indicate loading.
- Customizable via Tailwind classes for flexible size and shape.
- Can be used inline or as blocks in layouts.

## 🧪 Example

### Text Line Placeholder

```jsx
<Skeleton />
```

### Avatar Placeholder

```jsx
<Skeleton width="w-10" height="h-10" borderRadius="rounded-full" />
```

### Card Placeholder Block

```jsx
<div className="space-y-4">
  <Skeleton width="w-full" height="h-48" />
  <Skeleton width="w-1/2" height="h-6" />
  <Skeleton width="w-full" height="h-4" />
</div>
```

## 🧠 Notes

- It's just a `div` styled with Tailwind classes—no logic, no DOM updates.
- Combine multiple `Skeleton` components to build realistic loading UIs.
- Works great with conditional rendering to swap out real data once loaded.
