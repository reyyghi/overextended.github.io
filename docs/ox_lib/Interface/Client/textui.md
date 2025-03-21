---
title: TextUI
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

### lib.showTextUI

Show the TextUI window.

:::danger

**DO NOT** run this function every tick, it's intented to be used as a toggle.
:::

<Tabs>
<TabItem value='Lua'>

```lua
lib.showTextUI(text, options)
```

</TabItem>
<TabItem value='JS/TS'>

```ts
import lib from '@overextended/ox_lib/client'

lib.showTextUI(text, options)
```

</TabItem>
</Tabs>

* text: `string`
* options?: `table`
  * position?: `'right-center'` or `'left-center'` or `'top-center'`
    * Default: `'right-center'`
  * icon?: `string` or `table` (`array`)
  * iconColor?: `string`
  * style?: React.CSSProperties

### lib.hideTextUI

Hides the currently visible TextUI window

<Tabs>
<TabItem value='Lua'>

```lua
lib.hideTextUI()
```

</TabItem>
<TabItem value='JS/TS'>

```ts
import lib from '@overextended/ox_lib/client'

lib.hideTextUI()
```

</TabItem>
</Tabs>

### Usage Example

#### Basic

<Tabs>
<TabItem value='Lua'>

```lua
lib.showTextUI('[E] - Fuel vehicle')
```

</TabItem>
<TabItem value='JS/TS'>

```ts
import lib from '@overextended/ox_lib/client'

lib.showTextUI('[E] - Fuel vehicle')
```

</TabItem>
</Tabs>

![basic_example](https://i.imgur.com/uZS40fD.png)

#### Custom styling

<Tabs>
<TabItem value='Lua'>

```lua
lib.showTextUI('[E] - Pick apple', {
    position = "top-center",
    icon = 'hand',
    style = {
        borderRadius = 0,
        backgroundColor = '#48BB78',
        color = 'white'
    }
})
```

</TabItem>
<TabItem value='JS/TS'>

```ts
import lib from '@overextended/ox_lib/client'

lib.showTextUI('[E] - Pick apple', {
  position: "top-center",
  icon: 'hand',
  style: {
    borderRadius: 0,
    backgroundColor: '#48BB78',
    color: 'white'
  }
})
```

</TabItem>
</Tabs>

![custom_example](https://i.imgur.com/sy9lPC0.png)
