---
sidebar_position: 3
---

# CheckboxField

A styled and accessible checkbox input component built with Tailwind CSS, integrated with `react-hook-form`. Allows full customization through class overrides and displays validation errors.

## 📦 Import

```js
import { CheckboxField } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                      | Type        | Default      | Description |
|---------------------------|-------------|--------------|-------------|
| `label`                   | `string`    | — *(required)* | Text label shown next to the checkbox |
| `id`                      | `string`    | — *(required)* | The unique `id` for the checkbox input and label association |
| `register`                | `any`       | —            | `react-hook-form` register object |
| `errorMessage`            | `string`    | `undefined`  | Optional error message to display below the checkbox |
| `outerContainerClassName`| `string`    | `""`         | Custom class for the outermost wrapper `<div>` |
| `inputContainerClassName`| `string`    | `""`         | Custom class for the inner container holding input and label |
| `inputClassName`          | `string`    | `""`         | Custom class for the `<input type="checkbox">` |
| `labelClassName`          | `string`    | `""`         | Custom class for the checkbox label |
| `errorClassName`          | `string`    | `""`         | Custom class for the error `<p>` element |

## 💅 Styling Notes

- Checkbox base styles:
    - `h-4 w-4 rounded border-gray-300 text-blue-600`
    - Focus ring: `focus:ring-blue-500`
- Error state:
    - Error message styled as `text-red-500` by default

## 🧪 Example

```jsx
<CheckboxField
  id="agreeTerms"
  label="I agree to the terms and conditions"
  register={register("agreeTerms", { required: "You must agree to continue" })}
  errorMessage={errors.agreeTerms?.message}
/>
```

## 🧠 Tips

- Integrates seamlessly with `react-hook-form`'s validation.
- Ideal for consent checkboxes, feature toggles, or boolean form controls.
- Combine with `InputField` or `SelectField` for full form coverage.
