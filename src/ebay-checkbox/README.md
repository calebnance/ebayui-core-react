# EbayCheckbox

## Demo

[Storybook](https://opensource.ebay.com/ebayui-core-react/main/?path=/story/form-input-ebay-checkbox--default-checkbox-button)

## Install

```
yarn add @ebay/ui-core-react
```

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

| without extension | with extension |
| ----------------- | -------------- |
| <pre><code>import '@ebay/skin/checkbox'</code></pre> | <pre><code>import '@ebay/skin/checkbox.css'</code></pre> |

**Import Icons**

Add the below icons to the `<EbaySvg />` component.

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

| Name | Type | Default | Description |
|----- |------|---------|-------------|
| **size** | 'large' | 'regular' | String | `regular` | sets the checkbox icon size. For mweb this should be set to `large`. (Note: The dimensions of the radio will not change, but only the icon) |
| `disabled` | Boolean |
| `checked` | Boolean | | indicates the checked value of the input element, required for a controlled component. |
| `defaultChecked` | Boolean | | indicates the default checked input element value. Use when the component is not controlled. |
| `onChange` | Function | `(event: ChangeEvent, { value: string, checked: Boolean})` | callback fired on change |
| `onFocus` | Function |`(event: FocusEvent, { value: string, checked: Boolean })` | callback fired when button is focused |
| `onKeyDown` | Function | `(event: KeyboardEvent, { value: string, checked: Boolean })` | callback fired when key is pressed |

> [!NOTE]
> It supports all the events supported by an input element (e.g. `onClick`). For this component, `className`/`style` are applied to the root tag, while all other HTML attributes are applied to the `input` tag.