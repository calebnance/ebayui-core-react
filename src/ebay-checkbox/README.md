# EbayCheckbox

## Demo

[Storybook](https://opensource.ebay.com/ebayui-core-react/main/?path=/story/form-input-ebay-checkbox--default-checkbox-button)

## Install

For install and global requirements, please see our [Getting Started](../../README.md#getting-started) section.

## Usage (minimal)

**Import JS**

```jsx harmony
import {
    EbayCheckbox,
    type CheckboxChangeHandler,
    type CheckboxFocusHandler,
    type CheckboxKeyDownHandler
} from '@ebay/ui-core-react/ebay-checkbox'
```

**JSX**

```jsx harmony
<EbayCheckbox id="checkbox-1" />
```

**Import Styles**

```jsx harmony
import "@ebay/skin/checkbox";
```

> [!IMPORTANT]
> If tokens haven't been added to the project at a higher level, make sure to import

```jsx harmony
import "@ebay/skin/tokens";
```

**Import Icons**

Add the below icons to the `<EbaySvg />` component (added to the project at a higher level).

```tsx
<EbaySvg
    icons={[
        "checkboxChecked18",
        "checkboxUnchecked18",

        // If using large checkboxes
        "checkboxChecked24",
        "checkboxUnchecked24",
    ]}
/>
```

> [!NOTE]
> Make sure that `<EbaySvg />` is only rendered on the server so it does not affect the client bundle size.

## Usage (all props)

```jsx harmony
import {
    EbayCheckbox,
    type CheckboxChangeHandler,
    type CheckboxFocusHandler,
    type CheckboxKeyDownHandler
} from '@ebay/ui-core-react/ebay-checkbox'
import { EbayLabel } from '@ebay/ui-core-react/ebay-field';

<EbayCheckbox
    id="checkbox-1"
    checked={false}
    defaultChecked={false}
    disabled={false}
    size="regular"
    onChange={() => null}
    onKeyDown={() => null}
    onFocus={() => null}
>
    <EbayLabel>Remember me!</EbayLabel>
</EbayCheckbox>
```

## Attributes

| Name | Type | Required | Description |
| ---- | ---- | :------: | ----------- |
| `size` | `large` \| `regular`* \| String | No | sets the checkbox icon size. For mweb this should be set to `large`. (Note: The dimensions of the radio will not change, but only the icon) |
| `disabled` | Boolean | No |
| `checked` | Boolean | No | indicates the checked value of the input element, required for a controlled component. |
| `defaultChecked` | Boolean | No | indicates the default checked input element value. Use when the component is not controlled. |
| `onChange` | Function | No | callback fired on change: `(event: ChangeEvent, { value: string, checked: Boolean})` |
| `onFocus` | Function | No | callback fired when button is focused: `(event: FocusEvent, { value: string, checked: Boolean })` |
| `onKeyDown` | Function | No | callback fired when key is pressed: `(event: KeyboardEvent, { value: string, checked: Boolean })` |

> [!NOTE]
> It supports all the events supported by an input element (e.g. `onClick`). For this component, `className`/`style` are applied to the root tag, while all other HTML attributes are applied to the `input` tag.