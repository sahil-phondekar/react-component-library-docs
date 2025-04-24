---
sidebar_position: 7
---

# FileUploadField

A styled file upload input designed for form integration with `react-hook-form`. It allows users to select files and displays validation errors as needed. The component uses Tailwind CSS for styling and is highly customizable.

## 📦 Import

```js
import { FileUploadField } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                      | Type        | Default     | Description |
|---------------------------|-------------|-------------|-------------|
| `label`                   | `string`    | —           | Optional label displayed above the input |
| `id`                      | `string`    | — *(required)* | Unique identifier for the input |
| `accept`                  | `string`    | —           | Specifies the file types that can be uploaded (e.g., `image/*`, `.pdf`) |
| `register`                | `function`  | — *(required)* | `react-hook-form`'s register method |
| `errorMessage`            | `string`    | `undefined` | Displays a validation error below the input |
| `outerContainerClassName` | `string`    | `""`        | Class name for the outer wrapper |
| `inputClassName`          | `string`    | `""`        | Class name for the input element |
| `labelClassName`          | `string`    | `""`        | Class name for the label element |
| `errorClassName`          | `string`    | `""`        | Class name for the error message element |

## 💅 Styling Notes

- **Default styling**:
    - `w-full file:mr-4 file:py-2 file:px-4 file:rounded-lg file:border-0 file:text-sm file:font-semibold file:bg-blue-50 file:text-blue-700 hover:file:bg-blue-100`
- **Error message**:
    - `text-red-500 text-sm mt-1`

## 🧪 Example

```jsx
<FileUploadField
  id="profilePicture"
  label="Upload Profile Picture"
  accept="image/*"
  register={register("profilePicture", { required: "File is required" })}
  errorMessage={errors.profilePicture?.message}
/>
```

## 🧠 Tips

- Use the `accept` prop to restrict file types (e.g., `accept="image/*"` for images).
- Customize the file input's appearance with `file:` utility classes provided by Tailwind CSS.
