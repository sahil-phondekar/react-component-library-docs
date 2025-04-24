---
sidebar_position: 2
---

# Tabs

A flexible, customizable tab component that supports both horizontal and vertical tab layouts. It allows for easy creation of tabbed interfaces where users can switch between different sections of content.

## 📦 Import

```js
import { Tabs } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                   | Type                           | Default          | Description |
|------------------------|--------------------------------|------------------|-------------|
| `tabs`                  | `Array<Object>`                | — *(required)*   | Array of objects representing each tab. Each object should contain a `label` (string) and `content` (node) |
| `defaultIndex`          | `number`                       | `0`              | Index of the tab to be active by default |
| `direction`             | `string`                       | `"horizontal"`   | The direction of the tabs, either `"horizontal"` or `"vertical"` |
| `className`             | `string`                       | `""`             | Class name for the outer container |
| `tabClassName`          | `string`                       | `""`             | Class name for the tab button |
| `activeTabClassName`    | `string`                       | `""`             | Class name for the active tab |
| `contentClassName`      | `string`                       | `""`             | Class name for the content area |
| `fullWidth`             | `boolean`                      | `false`          | Whether the tabs should occupy the full width of the container |

## 🧩 Tabs Object

Each tab in the `tabs` array should follow this structure:

| Name        | Type              | Description |
|-------------|-------------------|-------------|
| `label`     | `string`          | The label to be displayed on the tab button |
| `content`   | `node`            | The content to be displayed when the tab is active |

## 🎨 Styling Notes

- **Tabs**: `px-4 py-2 text-sm font-medium focus:outline-none`
- **Active Tab**: Customizable with the `activeTabClassName` prop.
- **Tab Content**: `p-4 shadow` (Content is hidden for inactive tabs)
- **Tab Indicator**: A small indicator appears under the active tab. It is customizable based on the tab direction.

## 🧪 Example

```jsx
<Tabs
  tabs={[
    { label: "Tab 1", content: <div>Content for Tab 1</div> },
    { label: "Tab 2", content: <div>Content for Tab 2</div> },
    { label: "Tab 3", content: <div>Content for Tab 3</div> },
  ]}
  defaultIndex={0}
  direction="horizontal"
  className="my-tabs"
  tabClassName="tab-class"
  activeTabClassName="active-tab"
  contentClassName="content-class"
  fullWidth={false}
/>
```

## 🔄 Functionality

- **Tab Switching**: Clicking on a tab button changes the active tab. The corresponding content is displayed, and the other content is hidden.
- **Direction**: Supports both `horizontal` and `vertical` layouts for the tab buttons.
- **Full Width**: When set to `true`, each tab button occupies the full width of the container.

## 🧠 Tips

- Use `fullWidth` to create tab buttons that each take up equal space.
- Customize the active tab indicator using the `activeTabClassName` prop to match your design needs.
- For vertical tabs, you can control the spacing and layout with `isVertical` in the component's styling.
