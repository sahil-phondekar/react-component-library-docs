---
sidebar_position: 3
---

# DashboardLayout

A flexible layout component designed for dashboard-style UIs. It features a collapsible sidebar, mobile-friendly toggling, and main content area, providing an efficient structure for complex applications or admin dashboards.

## 📦 Import

```js
import { DashboardLayout } from "@sahilphondekar/react-component-library";
```

## 🧱 Props

| Name                     | Type                                                       | Default          | Description                                                                                             |
|--------------------------|------------------------------------------------------------|------------------|---------------------------------------------------------------------------------------------------------|
| `children`                | `ReactNode`                                                | **Required**     | The main content of the layout (e.g., dashboard content).                                               |
| `containerClassName`      | `string`                                                   | `""`             | Additional custom class names for the container.                                                       |
| `sidebarClassName`        | `string`                                                   | `""`             | Custom class names for the sidebar.                                                                     |
| `sidebarHeader`           | `ReactNode`                                                | `"Menu"`         | The text or component to display as the sidebar header.                                                 |
| `sidebarHeaderCollapsed`  | `ReactNode`                                                | `"M"`            | The collapsed sidebar header, shown when the sidebar is collapsed.                                      |
| `sidebarHeaderClassName`  | `string`                                                   | `""`             | Additional custom class names for the sidebar header.                                                  |
| `sidebarCollapsedIcon`    | `ReactNode`                                                | `<span className="block w-6 h-6">&gt;</span>` | Icon for collapsed state of the sidebar.                                                               |
| `sidebarOpenIcon`         | `ReactNode`                                                | `<span className="block w-6 h-6">&lt;</span>` | Icon for expanded state of the sidebar.                                                                |
| `sidebarContent`          | `ReactNode`                                                | **Required**     | The content inside the sidebar (typically navigation links).                                           |
| `sidebarContentClassName` | `string`                                                   | `""`             | Custom class names for the sidebar content.                                                            |
| `isSidebarCollapsed`      | `boolean`                                                  | `false`          | Controls whether the sidebar is collapsed.                                                             |
| `setIsSidebarCollapsed`   | `function`                                                 | `() => {}`       | Callback function to toggle the sidebar collapse state.                                                |
| `mainContentClassName`    | `string`                                                   | `""`             | Additional class names for the main content area.                                                      |
| `collapsible`             | `boolean`                                                  | `true`           | Controls whether the sidebar can be collapsed.                                                         |
| `sidebarWidth`            | `string`                                                   | `"w-64"`         | Width of the sidebar when expanded.                                                                    |
| `collapsedSidebarWidth`   | `string`                                                   | `"w-20"`         | Width of the sidebar when collapsed.                                                                   |
| `mobileBreakpoint`        | `number`                                                   | `768`            | The breakpoint for mobile views, below which the sidebar is fully collapsible.                          |

## ✨ Features

- **Collapsible Sidebar:** Can be toggled between collapsed and expanded states.
- **Mobile-Friendly:** Sidebar automatically adjusts on mobile and can be toggled via a button.
- **Customizable Sidebar and Content:** Offers customizable sidebar content, header, and layout for flexible dashboard designs.
- **Responsiveness:** Uses a breakpoint to adjust the layout for mobile users, with a mobile overlay when the sidebar is open.
- **Smooth Transitions:** Animations for opening/closing the sidebar and transitioning between states.

## 🧪 Examples

### Basic Usage

```jsx
<DashboardLayout sidebarContent={<div>Sidebar Content</div>}>
  <div>Main Content</div>
</DashboardLayout>
```

### Collapsible Sidebar with Custom Icons

```jsx
<DashboardLayout
  sidebarContent={<div>Sidebar Content</div>}
  sidebarOpenIcon={<span>&lt;</span>}
  sidebarCollapsedIcon={<span>&gt;</span>}
>
  <div>Main Content</div>
</DashboardLayout>
```

### Mobile View with Sidebar Toggle

```jsx
<DashboardLayout
  isSidebarCollapsed={false}
  sidebarContent={<div>Sidebar Content</div>}
>
  <div>Main Content</div>
</DashboardLayout>
```

## 🧠 Notes

- The `isSidebarCollapsed` prop is useful for controlling whether the sidebar is collapsed on page load.
- On mobile, the sidebar can be toggled using the hamburger icon. When open, the overlay ensures the main content is not clickable.
- The `collapsible` prop allows enabling/disabling the collapse feature for the sidebar.
