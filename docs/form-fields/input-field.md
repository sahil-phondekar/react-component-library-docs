---
sidebar_position: 1
---

# InputField

A customizable input component integrated with `react-hook-form` that supports error states, labels, and Tailwind CSS class overrides.

## 📦 Import

```js
import { InputField } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                     | Type        | Default     | Description |
|--------------------------|-------------|-------------|-------------|
| `label`                  | `string`    | `undefined` | Label text shown above the input |
| `id`                     | `string`    | — *(required)* | Unique ID for the input and associated label |
| `type`                   | `string`    | `"text"`    | Input type (e.g., `"text"`, `"email"`, `"password"`) |
| `register`               | `any`       | —           | `react-hook-form` register prop for form validation |
| `errorMessage`           | `string`    | `undefined` | Displays error message below input |
| `outerContainerClassName`| `string`    | `""`        | Additional classes for outer wrapper div |
| `inputClassName`         | `string`    | `""`        | Additional classes for the input element |
| `labelClassName`         | `string`    | `""`        | Additional classes for the label element |
| `errorClassName`         | `string`    | `""`        | Additional classes for the error message |

## 💅 Styling Notes

- **Default border:** `gray-300`
- **Error border:** `red-500`
- **Focus ring:** `blue-500` (normal), `red-500` (on error)
- Uses Tailwind CSS for styling.

## 🧪 Example

```jsx
<InputField
  id="email"
  label="Email Address"
  type="email"
  register={register("email", { required: "Email is required" })}
  errorMessage={errors.email?.message}
/>
```

## 🧠 Tips

- Use with `react-hook-form` for easy validation integration.
- Add `aria-invalid` or similar props for advanced accessibility needs if desired.
- Combine with components like `FormGroup`, `FormLabel`, etc., if building extended form patterns.
