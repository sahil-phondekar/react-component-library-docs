---
sidebar_position: 9
---

# TypeAheadSelectField

A customizable `react-select` powered dropdown with search functionality, integrated with `react-hook-form`. Supports label, error message display, and Tailwind CSS class overrides.

## 📦 Import

```js
import { TypeAheadSelectField } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                     | Type        | Default      | Description |
|---------------------------|-------------|--------------|-------------|
| `label`                   | `string`    | `undefined`  | Optional label text shown above the dropdown |
| `id`                      | `string`    | — *(required)* | Unique `id` for the input field and label |
| `options`                 | `Array<{ label: string, value: string }>` | — *(required)* | Options available for selection |
| `control`                 | `any`       | —            | `react-hook-form` control object (passed for consistency, but internally handled by Controller) |
| `errorMessage`            | `string`    | `undefined`  | Displays error message below the dropdown if provided |
| `outerContainerClassName` | `string`    | `""`         | Extra classes for the outer wrapper `<div>` |
| `labelClassName`          | `string`    | `""`         | Extra classes for the `<label>` element |
| `selectClassName`         | `string`    | `""`         | Extra classes for the `react-select` component |
| `errorClassName`          | `string`    | `""`         | Extra classes for the error `<p>` element |
| `placeholder`             | `string`    | `"Select..."` | Placeholder text shown when no option is selected |
| `...rest`                 | `any`       | —            | Any additional props are spread to `react-select` |

## 💅 Styling Notes

- Uses `react-select` under the hood with Tailwind-compatible class overrides.
- Default `react-select` style classes applied via `classNamePrefix="react-select"`.
- Error state highlights the select input with a `border-red-500` color.

## 🧪 Example

```jsx
import { Controller } from "react-hook-form";

const country = [
    {label: "India", value:"IN"},
    {label: "USA", value:"USA"},
];

<Controller
    defaultValue="IN"
    name="country"
    control={control}
    render={({ field }) => (
        <TypeAheadSelectField
            id="country"
            label="Country"
            options={country}
            {...field}
            value={country.find(c => c.value === field.value)}
            onChange={val => field.onChange(val.value)}
            errorMessage={errors.country?.message}
        />
    )}
/>

```

## 🧠 Tips

- Great for searchable dropdowns where users can quickly find options by typing.
- Works seamlessly with `Controller` from `react-hook-form`.
- You can fully customize the behavior and appearance of the dropdown using additional props supported by `react-select`.
