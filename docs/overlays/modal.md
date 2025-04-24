---
sidebar_position: 1
---

# Modal

The `Modal` component renders a responsive and accessible dialog overlay. It supports dynamic sizing, escape key handling, customizable content, and more.

## 📦 Import

```js
import { Modal } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                 | Type                          | Default      | Description |
|----------------------|-------------------------------|--------------|-------------|
| `isOpen`             | `boolean`                     | **Required** | Whether the modal is open. |
| `onClose`            | `function`                    | **Required** | Function to call when closing the modal. |
| `title`              | `ReactNode`                   | `undefined`  | Optional modal header title. |
| `children`           | `ReactNode`                   | **Required** | Content to display inside the modal. |
| `className`          | `string`                      | `""`         | Tailwind classes for modal container. |
| `size`               | `"sm"` \| `"md"` \| `"lg"` \| `"xl"` | `"md"`        | Controls the modal width. |
| `closeOnOverlayClick`| `boolean`                     | `true`       | Whether clicking outside closes the modal. |
| `showCloseButton`    | `boolean`                     | `true`       | Whether to show the top-right close button. |
| `overlayClassName`   | `string`                      | `""`         | Custom Tailwind classes for the modal overlay. |

## ✨ Features

- Accessible with keyboard (ESC key support)
- Custom overlay and modal styling
- Close on outside click (optional)
- Automatically disables background scroll when open
- Supports responsive max widths via `size` prop
- Close button with screen-reader label

## 🧪 Example

### Basic Usage

```jsx
<Modal
  isOpen={isModalOpen}
  onClose={() => setModalOpen(false)}
  title="Confirmation"
>
  <p>Are you sure you want to proceed?</p>
</Modal>
```

### With Custom Size and No Close Button

```jsx
<Modal
  isOpen={true}
  onClose={() => {}}
  title="Large Modal"
  size="lg"
  showCloseButton={false}
>
  <p>This modal doesn’t have a close button.</p>
</Modal>
```

## 🧠 Notes

- Ensure you handle `onClose` to update `isOpen` correctly in your parent component.
- The modal scrolls internally if content exceeds 80% of the viewport height.
- Don’t forget to stop propagation on the modal itself to prevent closing when clicking inside the content.
