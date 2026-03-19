<p align="left">
    <img width="1280" height="192" alt="DeclareUI" src="https://github.com/user-attachments/assets/d51c038f-7822-4ee4-beb8-f438894f7736#gh-light-mode-only" />
    <img width="1280" height="192" alt="DeclareUI" src="https://github.com/user-attachments/assets/44918531-3b1b-4ace-bca0-db0ea99f8bc8#gh-dark-mode-only" />
</p>

# @declareui/components

Official component library — 20+ production-ready UI components declared in YAML, compiled to any framework.

---

## What it does

A curated set of commonly-used UI components, declared once in `.ui.yaml` and ready to compile for React, Vue, Angular, Svelte, Web Components, or vanilla JS/TS.

## Installation

```bash
pnpm add @declareui/components
```

## Available components

| Category | Components |
|:---------|:-----------|
| **Actions** | Button, IconButton, Toggle, DropdownMenu |
| **Forms** | Input, Textarea, Select, Checkbox, Radio, Switch |
| **Layout** | Card, Container, Stack, Grid, Divider |
| **Feedback** | Alert, Badge, Toast, Tooltip, Progress |
| **Navigation** | Tabs, Breadcrumb, Pagination |
| **Data** | Avatar, Table, DataTable |

## Usage

```bash
# Copy components into your project
declareui add button card input

# Or build directly from the library
declareui build --from @declareui/components --targets react,vue
```

Each component follows DeclareUI conventions:

```yaml
# Example: button.ui.yaml
component: Button
props:
  variant:
    type: enum
    values: [primary, secondary, ghost, destructive]
    default: primary
  size:
    type: enum
    values: [sm, md, lg]
    default: md
  label:
    type: string
    required: true
template:
  tag: button
  classes:
    base: "inline-flex items-center justify-center rounded-lg font-medium"
    variants:
      variant:
        primary: "bg-blue-600 text-white hover:bg-blue-700"
        secondary: "bg-gray-100 text-gray-900 hover:bg-gray-200"
```

## Related packages

| Package | Description |
|:--------|:------------|
| [`@declareui/core`](https://github.com/declare-ui/core) | Parser, AST, and code generators |
| [`@declareui/tailwind-plugin`](https://github.com/declare-ui/tailwind-plugin) | Tailwind CSS integration |
| [`@declareui/cli`](https://github.com/declare-ui/cli) | CLI tool |

## Contributing

See [CONTRIBUTING.md](https://github.com/declare-ui/.github/blob/main/CONTRIBUTING.md) for guidelines.

## License

MIT
