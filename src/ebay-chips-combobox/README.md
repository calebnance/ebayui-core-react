# EbayChipsCombobox

## Demo

[Storybook](https://opensource.ebay.com/ebayui-core-react/main/?path=/docs/form-input-ebay-chips-combobox--docs)

## Install

For install and global requirements, please see our [Getting Started](../../README.md#getting-started) section.

## Usage (minimal)

**Import JS**

```jsx harmony
import { EbayChipsCombobox, EbayComboboxOption } from "@ebay/ui-core-react/ebay-chips-combobox";
```

**JSX**

```jsx harmony
<EbayChipsCombobox onChange={() => null}>
    <EbayComboboxOption text="Option 1" />
    <EbayComboboxOption text="Option 2" />
    <EbayComboboxOption text="Option 3" />
</EbayChipsCombobox>
```

**Import Styles**

```jsx harmony
import "@ebay/skin/combobox";
import "@ebay/skin/chip";
import "@ebay/skin/chips-combobox";
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

> [!NOTE]
> Make sure that `<EbaySvg />` is only rendered on the server so it does not affect the client bundle size.

## Usage (all props)

```jsx harmony
import { EbayChipsCombobox, EbayComboboxOption } from "@ebay/ui-core-react/ebay-chips-combobox";

<EbayChipsCombobox
    a11yDeleteButtonText="Remove item"
    className="chips-12"
    defaultSelected={['Option 1']}
    disabled={false}
    error={false}
    fluid
    onChange={() => null}
    placeholder="Select options"
>
    <EbayComboboxOption text="Option 1" />
    <EbayComboboxOption text="Option 2" />
    <EbayComboboxOption text="Option 3" />
</EbayChipsCombobox>
```

## Attributes

| Name | Type | Required | Description |
| ---- | ---- | :------: | ----------- |
| `a11yDeleteButtonText` | String | No | Accessibility text for the delete button |
| `className` | String | No | Ability to add class to container span |
| `defaultSelected` | Array | No | Array of strings, that are selected on load |
| `disabled` | Boolean | No |
| `error` | Boolean | No |
| `fluid` | Boolean | No | if true, css `display` is set to `block` instead of `inline-block` |
| `onChange` | Function | No | Triggered when the selection changes |
| `placeholder` | String | No | If no options selected, placeholder text is set in input |

> [!NOTE]
> The `<EbayChipsCombobox />` supports the same attributes as the [EbayCombobox](../ebay-combobox/README.md), with additional attributes specific to the chips functionality.