---
sidebar_position: 4
---

# CheckboxGroupField

A flexible group of checkboxes, designed for multiple selection fields and easily integrated with `react-hook-form`. Fully customizable with Tailwind utility overrides and displays inline error messaging.

## 📦 Import

```js
import { CheckboxGroupField } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                        | Type        | Default     | Description |
|-----------------------------|-------------|-------------|-------------|
| `label`                     | `string`    | —           | Optional group label displayed above the checkboxes |
| `name`                      | `string`    | — *(required)* | The name key used by `react-hook-form` |
| `options`                   | `array`     | — *(required)* | List of checkbox options, each with `{ label, value }` |
| `register`                  | `function`  | — *(required)* | `react-hook-form` register method |
| `errorMessage`              | `string`    | `undefined` | Error message for validation feedback |
| `outerContainerClassName`   | `string`    | `""`        | Class for the outermost wrapper `<div>` |
| `inputContainerClassName`   | `string`    | `""`        | Class for the wrapper around all checkboxes |
| `inputClassName`            | `string`    | `""`        | Class for each `<input type="checkbox">` |
| `labelClassName`            | `string`    | `""`        | Class for the group label |
| `optionLabelClassName`      | `string`    | `""`        | Class for each label next to a checkbox |
| `errorClassName`            | `string`    | `""`        | Class for the error message `<p>` |

## 💅 Styling Notes

- Checkboxes:
    - `h-4 w-4 text-blue-600 border-gray-300`
    - Focus ring on selection: `focus:ring-blue-500`
    - Error styles: `border-red-500 focus:ring-red-500`
- Group layout: `space-y-2 space-x-2` with inline-flex styling per option

## 🧪 Example

```jsx
<CheckboxGroupField
  name="interests"
  label="Select your interests"
  options={[
    { label: "Music", value: "music" },
    { label: "Travel", value: "travel" },
    { label: "Reading", value: "reading" },
  ]}
  register={register("interests", {
    validate: (value) => value.length > 0 || "Select at least one option",
  })}
  errorMessage={errors.interests?.message}
/>
```

## 🧠 Tips

- Best suited for multiple checkbox values under one field name.
- Combine with `InputField` and `SelectField` for complete form solutions.
- Works great with Tailwind-based responsive forms.