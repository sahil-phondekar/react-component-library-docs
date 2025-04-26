---
sidebar_position: 3
---

# ActionButtonList

The `ActionButtonList` component renders a dropdown menu of action buttons, triggered by an icon. Ideal for context menus, inline action lists, and compact UI elements.

## 📦 Import

```js
import { ActionButtonList } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                 | Type                                                                 | Default     | Description                                             |
|----------------------|----------------------------------------------------------------------|-------------|---------------------------------------------------------|
| `actions`            | `Array<{ icon: node, label: string, onClick: function }>`            | **Required**| List of actions with icon, label, and click handler     |
| `menuIcon`           | `node`                                                               | **Required**| Icon element that triggers the menu                     |
| `position`           | `"left"` \| `"right"` \| `"top"` \| `"bottom"`                       | `"left"`    | Position of the dropdown relative to the trigger button |
| `menuIconClassName`  | `string`                                                             | `""`        | Custom classes for the menu icon button                 |
| `menuClassName`      | `string`                                                             | `""`        | Custom classes for the dropdown container               |
| `containerClassName` | `string`                                                             | `""`        | Custom classes for the dropdown outer container         |
| `actionClassName`    | `string`                                                             | `""`        | Custom classes for each individual action               |

## 📍 Positions

| Position | Description                                |
|----------|--------------------------------------------|
| `left`   | Menu appears to the left of the trigger    |
| `right`  | Menu appears to the right of the trigger   |
| `top`    | Menu appears above the trigger             |
| `bottom` | Menu appears below the trigger             |

## 🚀 Examples

### Basic Usage

```jsx
<ActionButtonList
  menuIcon={<MoreVertical />}
  actions={[
    {
      icon: <Edit size={16} />,
      label: "Edit",
      onClick: () => alert("Edit clicked"),
    },
    {
      icon: <Trash2 size={16} />,
      label: "Delete",
      onClick: () => alert("Delete clicked"),
    },
  ]}
/>
```

### Right-Aligned Menu

```jsx
<ActionButtonList
  position="right"
  menuIcon={<MoreVertical />}
  actions={[
    {
      icon: <Eye />,
      label: "View",
      onClick: () => console.log("View"),
    },
  ]}
/>
```

### Custom Styling

```jsx
<ActionButtonList
  menuIcon={<MoreVertical />}
  menuIconClassName="text-blue-600"
  menuClassName="bg-gray-100 border border-gray-200"
  actionClassName="text-sm text-gray-900"
/>
```

## 💡 Best Practices

- Keep the number of actions limited for better usability.
- Use descriptive labels and icons to clearly convey action intent.
- Combine `position` and spacing utilities for precise dropdown placement.
- Ensure dropdown content is keyboard accessible (coming soon in ARIA enhancements).
