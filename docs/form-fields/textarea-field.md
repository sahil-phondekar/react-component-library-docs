---
sidebar_position: 8
---

# TextAreaField

A styled textarea input for forms, designed to integrate seamlessly with `react-hook-form`. It provides built-in support for validation errors and customizable styling.

## 📦 Import

```js
import { TextareaField } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                      | Type        | Default     | Description |
|---------------------------|-------------|-------------|-------------|
| `label`                   | `string`    | —           | Optional label displayed above the textarea |
| `id`                      | `string`    | — *(required)* | Unique identifier for the textarea |
| `register`                | `function`  | — *(required)* | `react-hook-form`'s register method |
| `errorMessage`            | `string`    | `undefined` | Validation error message displayed below the textarea |
| `rows`                    | `number`    | `4`         | Number of rows for the textarea (default is 4) |
| `outerContainerClassName` | `string`    | `""`        | Class name for the outer wrapper |
| `inputClassName`          | `string`    | `""`        | Class name for the textarea element |
| `labelClassName`          | `string`    | `""`        | Class name for the label element |
| `errorClassName`          | `string`    | `""`        | Class name for the error message element |

## 💅 Styling Notes

- **Default styling**:
    - `w-full px-3 py-2 border rounded-lg resize-none focus:outline-none`
- **Error message**:
    - `text-red-500 text-sm mt-1`

## 🧪 Example

```jsx
<TextareaField
  id="description"
  label="Description"
  rows={6}
  register={register("description", { required: "Description is required" })}
  errorMessage={errors.description?.message}
/>
```

## 🧠 Tips

- The `rows` prop allows you to control the height of the textarea. The default value is 4.
- You can customize the textarea's appearance using `inputClassName` and other props.
