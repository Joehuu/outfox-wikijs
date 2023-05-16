---
title: DeviceList
weight: 0
geekdocCollapseSection: true
---

A [BitmapText](../bitmaptext/) actor that shows the current list of devices connected and recognized by the game.

```lua
Def.DeviceList {
	Font="Common Normal"
}
```

This actor is used on the Test Input screen to showcase which controllers are detected.

Attributes for this actor can be found on [BitmapText](../bitmaptext/).

{{<hint type="important">}}
Text application to this actor is ignored as the game automatically updates it with the current devices.
{{</hint>}}