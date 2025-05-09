---
sidebar_position: 10
---

# AsyncTypeAheadSelectField

An asynchronous `react-select/async` powered searchable dropdown that fetches options dynamically. Supports label, error message display, and Tailwind CSS class overrides.

## 📦 Import

```js
import { AsyncTypeAheadSelectField } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                     | Type        | Default      | Description |
|---------------------------|-------------|--------------|-------------|
| `label`                   | `string`    | `undefined`  | Optional label text shown above the dropdown |
| `id`                      | `string`    | — *(required)* | Unique `id` for the input field and label |
| `loadOptions`             | `(inputValue: string) => Promise<Array<{ label: string, value: string }>>` | — *(required)* | Async function to load options based on user input |
| `control`                 | `any`       | —            | `react-hook-form` control object (passed for consistency, handled via Controller) |
| `errorMessage`            | `string`    | `undefined`  | Displays error message below the dropdown if provided |
| `outerContainerClassName` | `string`    | `""`         | Extra classes for the outer wrapper `<div>` |
| `labelClassName`          | `string`    | `""`         | Extra classes for the `<label>` element |
| `selectClassName`         | `string`    | `""`         | Extra classes for the `react-select` component |
| `errorClassName`          | `string`    | `""`         | Extra classes for the error `<p>` element |
| `placeholder`             | `string`    | `"Select..."` | Placeholder text shown when no option is selected |
| `...rest`                 | `any`       | —            | Any additional props are spread to `AsyncSelect` |

## 💅 Styling Notes

- Built on top of `react-select/async` with Tailwind-compatible class overrides.
- Default `react-select` class prefix applied via `classNamePrefix="react-select"`.
- Error state highlights the select input with a `border-red-500` color.

## 🧪 Example

```jsx
import { Controller } from "react-hook-form";

const loadOptions = async (inputValue) => {
    if (!inputValue) return [];

    try {
        const response = await fetch(
            `https://jsonplaceholder.typicode.com/users`
        );
        const users = await response.json();

        // Filter users by inputValue (simulate backend search)
        const filtered = users.filter((user) =>
            user.name.toLowerCase().includes(inputValue.toLowerCase())
        );

        // Map to react-select format
        return filtered.map((user) => ({
            label: user.name,
            value: user.id,
        }));
    } catch (error) {
        console.error("Error fetching users:", error);
        return [];
    }
};

<Controller
  name="users"
  control={control}
  render={({ field }) => (
    <AsyncTypeAheadSelectField
      id="users"
      label="Users (Async)"
      loadOptions={loadOptions}
      {...field}
      value={undefined}
      onChange={val => field.onChange(val?.value)}
      errorMessage={errors.users?.message}
    />
  )}
/>
```

## 🧠 Tips

- Ideal for large datasets where you don't want to load all options at once.
- Works great with paginated APIs or search endpoints.
- Use `cacheOptions` and `defaultOptions` for better user experience with async loading.

