---
title: SongBPMDisplay
description: A slightly automated version of BPMDisplay that automatically updates the text to the BPM range from a given player.
published: true
date: 2023-05-20T20:47:20.596Z
tags: actor, songbpmdisplay
editor: markdown
dateCreated: 2023-05-16T06:15:56.392Z
---

A slightly automated version of [BPMDisplay](/en/dev/actors/actortypes/bpmdisplay) that automatically updates the text to the BPM range from a given player.

```lua
Def.SongBPMDisplay{
	Player = PLAYER_1,
}
```

## Attributes

| Name | Type | Action |
| :--- | :--- | :----- |
Player | PlayerNumber | The player to obtain the current BPM from.

This actor inherits the attributes from [BitmapText](/en/dev/actors/actortypes/bitmaptext).

## Functions

> These functions also work on [BPMDisplay](../bpmdisplay/).
{.is-info}

### `SetFromGameState`

Obtains the current BPM information from the song or course.
If the song is from an extra stage, it will report it as a random value instead.

### `SetFromSong`
`(Song pSong)`

Sets the BPM to the song's BPM range. This value can be tricked if the chart is using a specified BPM rather than the actual BPM,
or even jumbled if it's tagged as random.

### `SetFromSteps`
`(Steps data)`

Sets the BPM to the steps's BPM range. Useful if the current steps contain different timing data.

### `SetFromCourse`
`(Course pCourse)`

Obtains the BPM range from the course. A couple of rules are applied here:

- The operation will fail if there are no steps available on the course for the current StepsType.
- If there are more entries than the value of `Common::MaxCourseEntriesBeforeShowVarious` (Default: `10`), the course is considered **various**, and instead
will output the text defined on `BPMDisplay::VariousText` (Default: `"000"`).

### `GetText`

Gets the current value that the SongBPMDisplay contains.