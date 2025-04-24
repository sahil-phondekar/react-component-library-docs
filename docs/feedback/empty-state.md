---
sidebar_position: 5
---

# EmptyState

The `EmptyState` component is used to inform users when there is no data to display. It supports customizable icons, titles, and descriptions to better match different use cases.

## 📦 Import

```js
import { EmptyState } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name         | Type                                   | Default               | Description |
|--------------|----------------------------------------|------------------------|-------------|
| `title`      | `string`                               | `"No Data Available"`  | The main heading displayed to the user. |
| `description`| `string`                               | `"There is no content to display."` | Secondary text below the title. |
| `icon`       | `string` or `ReactNode`                | `undefined`            | Optional icon, either an SVG string or a React component. |
| `iconSize`   | `"sm"`, `"md"`, `"lg"`                 | `"lg"`                 | Controls the icon size (sm = 48px, md = 64px, lg = 80px). |
| `iconColor`  | `string`                               | `"text-gray-400"`      | Tailwind text color classes applied to the icon. |
| `compact`    | `boolean`                              | `false`                | Applies smaller padding for more compact UI. |
| `className`  | `string`                               | `""`                   | Additional Tailwind utility classes. |

## ✨ Features

- Configurable title and description
- Supports both custom icons and string-based SVG icons
- Clean default layout with Tailwind CSS
- Optional compact variant for tighter UIs
- Great for “no data” states in tables, cards, or dashboards

## 🧪 Example

### Basic Usage

```jsx
<EmptyState />
```

### With Custom Title and Icon

```jsx
<EmptyState
  title="No Orders Yet"
  description="You haven’t received any orders."
  icon="<svg xmlns='http://www.w3.org/2000/svg' ... />"
/>
```

### With React Component Icon and Compact Mode

```jsx
import { InboxIcon } from "lucide-react";

<EmptyState
  title="Nothing Here"
  description="Please check back later."
  icon={<InboxIcon />}
  iconSize="md"
  compact
/>
```

## 🧠 Notes

- If you’re using an SVG string for the `icon`, it will be rendered using the internal `SvgIcon` component.
- The layout is centered and responsive by default.
