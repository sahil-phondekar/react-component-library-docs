---
sidebar_position: 5
---

# RadioGroupField

A customizable and accessible radio button group for single selection, fully integrated with `react-hook-form`. Designed with Tailwind classes and flexibility in mind, it provides clear error feedback and styling overrides.

## 📦 Import

```js
import { RadioGroupField } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                        | Type        | Default     | Description |
|-----------------------------|-------------|-------------|-------------|
| `label`                     | `string`    | —           | Optional group label displayed above the radios |
| `name`                      | `string`    | — *(required)* | Name of the field (used by `react-hook-form`) |
| `options`                   | `array`     | — *(required)* | List of radio options: `{ label, value }[]` |
| `register`                  | `function`  | — *(required)* | `react-hook-form` register method |
| `errorMessage`              | `string`    | `undefined` | Error message to display under the group |
| `outerContainerClassName`   | `string`    | `""`        | Additional class for outermost container |
| `inputContainerClassName`   | `string`    | `""`        | Class for the container wrapping the radio buttons |
| `inputClassName`            | `string`    | `""`        | Class applied to each radio input |
| `labelClassName`            | `string`    | `""`        | Class for the group label element |
| `optionLabelClassName`      | `string`    | `""`        | Class applied to the label for each radio option |
| `errorClassName`            | `string`    | `""`        | Class applied to the error message |

## 💅 Styling Notes

- **Base Inputs**:
    - Size: `h-4 w-4`
    - Color: `text-blue-600`
    - Focus: `focus:ring-blue-500`
- **Error State**:
    - `border-red-500 focus:ring-red-500`
- **Layout**:
    - Default horizontal/vertical spacing via `space-y-2 space-x-2`

## 🧪 Example

```jsx
<RadioGroupField
  name="gender"
  label="Select your gender"
  options={[
    { label: "Male", value: "male" },
    { label: "Female", value: "female" },
    { label: "Other", value: "other" },
  ]}
  register={register("gender", {
    required: "Please select a gender",
  })}
  errorMessage={errors.gender?.message}
/>
```

## 🧠 Tips

- Useful for any single-choice selection.
- For inline display, apply `flex` styles via `inputContainerClassName`.
- Combine with `InputField`, `CheckboxGroupField` for a complete form UI.
