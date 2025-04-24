---
sidebar_position: 2
---

# SelectField

A customizable and accessible `select` dropdown input integrated with `react-hook-form`. Supports label, error message, and Tailwind CSS class overrides.

## 📦 Import

```js
import { SelectField } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                      | Type        | Default      | Description |
|---------------------------|-------------|--------------|-------------|
| `label`                   | `string`    | `undefined`  | Optional label text shown above the dropdown |
| `id`                      | `string`    | — *(required)* | The unique `id` for the `<select>` element and its label |
| `options`                 | `Array<{ label: string, value: string }>` | — *(required)* | Options to show in the dropdown |
| `register`                | `any`       | —            | `react-hook-form` register object |
| `errorMessage`            | `string`    | `undefined`  | Displays error message below dropdown if provided |
| `outerContainerClassName`| `string`    | `""`         | Extra classes for the outer wrapper `<div>` |
| `inputClassName`          | `string`    | `""`         | Extra classes for the `<select>` element |
| `labelClassName`          | `string`    | `""`         | Extra classes for the `<label>` element |
| `optionLabelClassName`    | `string`    | `""`         | Extra classes for each `<option>` element |
| `errorClassName`          | `string`    | `""`         | Extra classes for the error `<p>` element |

## 💅 Styling Notes

- Uses Tailwind CSS for all base styles.
- Default appearance:
    - `border-gray-300` with `focus:ring-blue-500`
- Error state:
    - `border-red-500` with `focus:ring-red-500`

## 🧪 Example

```jsx
<SelectField
  id="country"
  label="Country"
  options={[
    { label: "India", value: "IN" },
    { label: "United States", value: "US" },
  ]}
  register={register("country", { required: "Country is required" })}
  errorMessage={errors.country?.message}
/>
```

## 🧠 Tips

- Useful for dropdown menus in forms.
- Works well with `InputField` to create complete form UIs.
- You can dynamically generate the `options` from an API or local constants.