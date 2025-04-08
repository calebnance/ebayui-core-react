# EbayCombobox

## Demo

[Storybook](https://opensource.ebay.com/ebayui-core-react/main/?path=/docs/form-input-ebay-combobox--docs)

## Install

For install and global requirements, please see our [Getting Started](../../README.md#getting-started) section.

## Usage (minimal)

**Import JS**

```jsx harmony
import { EbayCombobox, EbayComboboxOption } from "@ebay/ui-core-react/ebay-combobox";
```

**JSX**

```jsx harmony
<EbayCombobox>
    <EbayComboboxOption text="Option 1" />
    <EbayComboboxOption text="Option 2" />
    <EbayComboboxOption text="Option 3" />
</EbayCombobox>
```

**Import Styles**

```jsx harmony
import "@ebay/skin/combobox";
```

> [!IMPORTANT]
> If tokens haven't been added to the project at a higher level, make sure to import

```jsx harmony
import "@ebay/skin/tokens";
```

## Usage (all props)

```jsx harmony
import { EbayCombobox, EbayComboboxOption, EbayComboboxButton } from "@ebay/ui-core-react/ebay-combobox";
import { EbayIcon } from '@ebay/ui-core-react/ebay-icon';

import "@ebay/skin/combobox";
import '@ebay/skin/icon';
import '@ebay/skin/icon-button';

<EbayCombobox
    autocomplete="none"
    borderless={false}
    disabled={false}
    expanded={false}
    floatingLabel={false}
    fluid={false}
    onChange={(e, { currentInputValue, selectedOption: { text } }) => {
        console.log('change', e, currentInputValue, text);
    }}
    onCollapse={() => console.log('collapse')}
    onExpand={() => console.log('expanded')}
>
    <EbayComboboxButton>
        <EbayIcon name="clear16" />
    </EbayComboboxButton>

    <EbayComboboxOption text="Option 1" />
    <EbayComboboxOption text="Option 2" />
    <EbayComboboxOption text="Option 3" />
</EbayCombobox>
```

## Attributes

| Name | Type | Required | Description |
| ---- | ---- | :------: | ----------- |
| `borderless` | Boolean | No | whether button has borders |
| `disabled` | Boolean | No | sets the disabled attribute of the input |
| `expanded` | Boolean | No | sets whether the listbox is expanded |
| `autocomplete` | String | No | default is `none`; available values are `none` or `list`. For list, will automatically filter results while typing. |
| `listSelection` | Boolean | No | default is `automatic`; available values are `automatic`, `manual`. If set to automatic will automatically fill in the input with the currently highlighted item when using the up/down keys. |
| `floatingLabel` | Boolean | No | The label to show on the combobox which moves up when focused |
| `fluid` | Boolean | No | If true, combobox will span the entire width of it's container |

## Event Handlers

### `onChange`

same as the `onChange` event, which fires on blur

**Required**: No

**Parameters**:

```tsx
(
    event,
    { currentInputValue, selectedOption: { text }}
)
```

### `onInputChange`

same as the `onInpuChanget` event, which fires with every keypress

**Required**: No

**Parameters**:

```tsx
(
    event,
    { currentInputValue, selectedOption: { text } }
)
```

### `onSelect`

similar to a `<select>`, which fires when an option is clicked or selected

**Required**: No

**Parameters**:

```tsx
(
    event,
    { currentInputValue, selectedOption: { text } }
)
```

### `onFocus`

same as the `onFocus` event, which fires on focus

**Required**: No

**Parameters**:

```tsx
(
    event,
    { currentInputValue, selectedOption: { text } }
)
```

### `onCollapse`

combobox has been closed

### `onExpand`

combobox has been opened

### `onFloatingLabelInit`

when floating label finishes initializing

