# EbayChip

## Demo

[Storybook](https://opensource.ebay.com/ebayui-core-react/main/?path=/docs/building-blocks-ebay-chip--docs)

## Install

For install and global requirements, please see our [Getting Started](../../README.md#getting-started) section.

## Usage (minimal)

**Import JS**

```jsx harmony
import { EbayChip } from "@ebay/ui-core-react/ebay-chip";
```

**JSX**

```jsx harmony
<EbayChip
    a11yDeleteButtonText="Remove item"
    onDelete={() => null}
    disabled={false}
>
    Chip content
</EbayChip>
```

**Import Styles**

```jsx harmony
import "@ebay/skin/chip";
```

> [!IMPORTANT]
> If tokens haven't been added to the project at a higher level, make sure to import

```jsx harmony
import "@ebay/skin/tokens";
```

**Import Icons**

Add the below icon to the `<EbaySvg />` component (added to the project at a higher level).

```tsx
<EbaySvg
    icons={[
        "close12"
    ]}
/>
```

## Attributes

| Name                   | Type     | Required | Description                                |
| ---------------------- | -------- | :------: | ------------------------------------------ |
| `a11yDeleteButtonText` | String   | No       | Accessibility text for the delete button   |
| `onDelete`             | Function | Yes      | Triggered when the delete button is clicked|
| `disabled`             | Boolean  | No       | Whether the chip is disabled               |
