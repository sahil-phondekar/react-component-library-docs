---
sidebar_position: 1
---

# Table

A responsive, sortable, and paginated table component designed to display tabular data with features like sorting, pagination, custom row rendering, and error handling. Perfect for dynamic data tables in React.

## 📦 Import

```js
import { Table } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                            | Type                          | Default               | Description |
|----------------------------------|-------------------------------|-----------------------|-------------|
| `data`                           | `Array<Object>`               | `[]`                  | Array of data objects to display in the table |
| `columns`                        | `Array<Object>`               | `[]`                  | Array of column definitions |
| `pageSize`                       | `number`                      | `10`                  | Number of rows per page |
| `currentPage`                    | `number`                      | `1`                   | Current page number |
| `totalPages`                     | `number`                      | `1`                   | Total number of pages |
| `totalItems`                     | `number`                      | `0`                   | Total number of items in the data set |
| `sortBy`                         | `string`                      | `null`                | Column to sort by |
| `sortOrder`                      | `string`                      | `"asc"`               | Sort order ("asc" or "desc") |
| `isLoading`                      | `boolean`                     | `false`               | Whether the table is in loading state |
| `error`                          | `string`                      | `null`                | Error message to display |
| `onPageChange`                   | `function`                    | — *(required)*        | Callback function when page changes |
| `onSortChange`                   | `function`                    | — *(required)*        | Callback function when sorting changes |
| `className`                      | `string`                      | `""`                  | Class name for the outer container |
| `loader`                         | `node`                        | `"Loading.."`         | Loader text or component to display while loading |
| `errorClassName`                 | `string`                      | `""`                  | Class name for error message |
| `tableClassName`                 | `string`                      | `""`                  | Class name for the table |
| `tableHeaderClassName`           | `string`                      | `""`                  | Class name for table header |
| `tableRowClassName`              | `string`                      | `""`                  | Class name for table rows |
| `stripedRowClassName`            | `Array<string>`               | `["bg-gray-50", "bg-gray-100"]` | Class names for striped rows |
| `emptyState`                     | `string | node`                | `"No Data Found"`     | Message to display when no data is available |
| `emptyStateClassName`            | `string`                      | `""`                  | Class name for the empty state message |
| `paginationContainerClassName`   | `string`                      | `""`                  | Class name for pagination container |
| `paginationButtonClassName`      | `string`                      | `""`                  | Class name for pagination buttons |
| `paginationPagesClassName`       | `string`                      | `""`                  | Class name for pagination page number container |
| `paginationTextClassName`        | `string`                      | `""`                  | Class name for pagination text |
| `sortable`                       | `boolean`                     | `true`                | Whether columns are sortable |

## 🧅 Column Object

Each column in the `columns` array should follow this structure:

| Name            | Type              | Description |
|-----------------|-------------------|-------------|
| `header`        | `string`          | The header label for the column |
| `accessor`      | `string`          | The key in the data object to display in the column |
| `isSortable`    | `boolean`         | If true, the column is sortable |
| `cellRenderer`  | `function`        | Custom renderer for the cell |

## 💅 Styling Notes

- **Table**: `min-w-full border-collapse`
- **Headers**: `p-1 font-medium text-gray-700 text-sm`
- **Rows**: `border-b text-sm` (with striped row colors alternating between `bg-gray-50` and `bg-gray-100`)
- **Pagination**: Customizable with classes for button and page elements.

## 🧪 Example

```jsx
<Table
  data={tableData}
  columns={[
    { header: "Name", accessor: "name", isSortable: true },
    { header: "Age", accessor: "age", isSortable: true },
    { header: "Email", accessor: "email" },
  ]}
  pageSize={10}
  currentPage={1}
  totalPages={5}
  totalItems={50}
  sortBy="name"
  sortOrder="asc"
  isLoading={false}
  error={null}
  onPageChange={handlePageChange}
  onSortChange={handleSortChange}
/>
```

## 🧠 Tips

- The `sortable` prop enables column sorting. Clicking on sortable column headers toggles between ascending and descending order.
- Use `cellRenderer` in column definitions to customize how data appears in each cell.
- The `pagination` component is fully customizable and includes buttons for navigation.
