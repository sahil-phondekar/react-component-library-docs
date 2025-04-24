---
sidebar_position: 6
---

# DateField

A styled and form-integrated date picker input built with Tailwind CSS and `react-hook-form`. This field handles validation styling, error display, and supports extensive customization via class overrides.

## 📦 Import

```js
import { DateField } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                      | Type        | Default     | Description |
|---------------------------|-------------|-------------|-------------|
| `label`                   | `string`    | —           | Optional label displayed above the input |
| `id`                      | `string`    | — *(required)* | Unique identifier for the input |
| `register`                | `function`  | — *(required)* | `react-hook-form`'s register method |
| `errorMessage`            | `string`    | `undefined` | Displays a validation error below the input |
| `outerContainerClassName` | `string`    | `""`        | Class name for outer wrapper |
| `inputClassName`          | `string`    | `""`        | Class name applied to the input element |
| `labelClassName`          | `string`    | `""`        | Class name for the label element |
| `errorClassName`          | `string`    | `""`        | Class name for the error message element |

## 💅 Styling Notes

- **Default styling**:
    - `w-full px-3 py-2 border rounded-lg text-sm`
- **Focus ring**:
    - Blue by default, red if `errorMessage` is provided
- **Error message**:
    - `text-red-500 text-sm mt-1`

## 🧪 Example

```jsx
<DateField
  id="dob"
  label="Date of Birth"
  register={register("dob", { required: "Date of birth is required" })}
  errorMessage={errors.dob?.message}
/>
```

## 🧠 Tips

- Works perfectly for birthdate fields, event dates, and date-based filters.
- Consider wrapping it with `min` or `max` attributes via `...rest` for date constraints.
