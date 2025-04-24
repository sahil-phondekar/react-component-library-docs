---
sidebar_position: 3
---

# Accordion

A collapsible accordion component to display expandable/collapsible content. It allows you to create a list of accordion items that can be toggled open and closed.

## 📦 Import

```js
import { Accordion } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                  | Type                                    | Default               | Description |
|-----------------------|-----------------------------------------|-----------------------|-------------|
| `items`               | `Array<Object>`                         | — *(required)*        | Array of objects representing each accordion item. Each object should contain a `title` (string) and `content` (node or string). |
| `allowMultiple`       | `boolean`                               | `false`               | Whether multiple items can be open simultaneously. |
| `defaultOpenFirst`    | `boolean`                               | `false`               | Whether the first item should be open by default. |
| `className`           | `string`                                | `""`                  | Class name for the outer container. |
| `itemClassName`       | `string`                                | `""`                  | Class name for each accordion item. |
| `titleClassName`      | `string`                                | `""`                  | Class name for the title button of each accordion item. |
| `contentClassName`    | `string`                                | `""`                  | Class name for the content of each accordion item. |
| `iconOpen`            | `string | ReactElement`                 | — *(optional)*        | SVG or React element representing the open icon. |
| `iconClosed`          | `string | ReactElement`                 | — *(optional)*        | SVG or React element representing the closed icon. |
| `iconSize`            | `string`                                | `"16px"`              | Size of the icons. |

## 🧩 `AccordionItem` Props

Each item in the `items` array should follow this structure:

| Name         | Type                               | Description |
|--------------|------------------------------------|-------------|
| `title`      | `string`                           | The title to be displayed in the accordion header. |
| `content`    | `node | string`                    | The content to be displayed when the accordion item is expanded. |
| `isOpen`     | `boolean`                          | Whether the accordion item is open. |
| `onToggle`   | `function`                         | Function to toggle the state of the accordion item. |
| `className`  | `string`                           | Custom class name for the accordion item. |
| `titleClassName` | `string`                         | Custom class name for the title button. |
| `contentClassName` | `string`                       | Custom class name for the content area. |
| `iconOpen`   | `string | ReactElement`            | SVG or React element for the open icon. |
| `iconClosed` | `string | ReactElement`            | SVG or React element for the closed icon. |
| `iconSize`   | `string`                           | Size of the open/closed icons. |

## 🎨 Styling Notes

- **Accordion Item**: Styled with border and shadow (`border border-gray-200 shadow-sm`).
- **Title Button**: `w-full text-left px-4 py-3 font-medium` (customizable).
- **Content**: `overflow-hidden transition-all duration-300` (content height is dynamically adjusted based on whether it's open or closed).
- **Icons**: You can customize the open/closed icons using the `iconOpen` and `iconClosed` props. Both `string` (SVG) and `ReactElement` types are supported.

## 🧪 Example

```jsx
<Accordion
  items={[
    { title: "Section 1", content: <div>Content for section 1</div> },
    { title: "Section 2", content: "This is some content for section 2" },
  ]}
  allowMultiple={true}
  defaultOpenFirst={true}
  iconSize="20px"
/>
```

## 🔄 Functionality

- **Accordion Toggle**: Each item can be expanded or collapsed by clicking on the title. The content is revealed/hidden with a smooth transition.
- **Multiple Open Items**: If `allowMultiple` is set to `true`, multiple accordion items can be open at once.
- **Icon Customization**: You can customize the open and closed icons for each item with the `iconOpen` and `iconClosed` props.
- **Dynamic Height**: The height of the content area dynamically adjusts to accommodate the content, and it transitions smoothly when opening/closing.

## 🧠 Tips

- Use `allowMultiple` if you want to enable multiple items to be open at the same time.
- Customize the open and closed icons to match your design by passing a string (SVG) or React element.
- You can pass any React node as the `content`, allowing flexibility for complex content.
