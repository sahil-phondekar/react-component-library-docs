---
sidebar_position: 4
---

# PlainLayout

A simple layout component that provides a basic wrapper for the main content of the page. It ensures that the content takes up the full height of the screen with minimal styling. Ideal for pages that don’t require a sidebar or advanced layout features.

## 📦 Import

```js
import { PlainLayout } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name               | Type         | Default     | Description                                                  |
|--------------------|--------------|-------------|--------------------------------------------------------------|
| `children`          | `ReactNode`  | **Required**| The main content to be rendered inside the layout.            |
| `containerClassName`| `string`     | `""`        | Additional custom class names for the layout container.       |

## ✨ Features

- **Full-Screen Layout:** Ensures the layout takes the full height of the screen.
- **Minimal Styling:** Provides a barebones container with customizable class names for the outer wrapper.
- **Customizable:** Easily extendable with additional custom styles.

## 🧪 Example Usage

```jsx
<PlainLayout>
  <div>Your main content goes here</div>
</PlainLayout>
```

### With Custom Class Names

```jsx
<PlainLayout containerClassName="bg-gray-100">
  <div>Your main content goes here</div>
</PlainLayout>
```

## 🧠 Notes

- The layout uses `min-h-screen` to ensure it stretches to the full height of the viewport.
- You can easily customize the outer container by passing a `containerClassName` prop.
