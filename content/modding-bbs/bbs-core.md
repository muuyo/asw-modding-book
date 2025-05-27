# How BBS works in-game

<hr>

## Generic states

The native code of the game looks for, and uses, several default states. This means the developers don't have to explicitly handle generic state transitions.
If a standing move ends, characters start looping `CmnActStand`. If a character gets hit, they'll go into the state that matches the hit reaction.

Native code is also able to affect script flow within those default states.
```bbs_o
ActionBegin: s32(CmnActJump) {
	Label: s32(_Upper)
	Label: s32(upperloop)
	CellBegin s32(kfs021_00), 3
	CellBegin s32(kfs021_01), 3
	CellBegin s32(kfs021_02), 3
	CellEnd:
	Goto: s32(upperloop)
	Label: s32(_UpperToTop)
	CellBegin s32(kfs021_03), 2
	CellBegin s32(kfs021_04), 2
	CellBegin s32(kfs022_00), 2
	CellBegin s32(kfs022_01), 2147483647
	Label: s32(_Top)
	CellBegin s32(kfs022_02), 2147483647
	Label: s32(_TopToDown)
	CellBegin s32(kfs022_03), 3
	CellBegin s32(kfs022_04), 2147483647
	Label: s32(_Down)
	Label: s32(downloop)
	CellBegin s32(kfs022_05), 3
	CellBegin s32(kfs022_06), 3
	CellBegin s32(kfs022_07), 3
	CellEnd:
	Goto: s32(downloop)
} ActionEnd:
```
As you can see, there are several different labels in this `CmnActJump` state, but you won't ever find a function that actually jumps to `_TopToDown`. Instead, the native code does so itself when the proper conditions are met (e.g. airborne, Y-speed less than 0).

Native code can also add function calls whenever it detects certain active state names. For example, DBFZ's `CmnActMikiwameMove` (Vanish) will initiate a worldStop, even if all relevant calls in the script have been deleted.

## Generic subroutines

Native code is also able to call a subroutine for an object of its own accord. Here are a few notable ones:

| Subroutine | Functionality |
| ----------------------------- | ----------------------------- |
| `OnIdling` | Called every game tick, no matter which state the object is in.<br />Affected by worldStop. |
| `OnLanding` |  |
| `OnDamage`|  |
| `OnGuard` |  |
| `OnFrameStep` | Called every game tick, no matter which state the object is in.<br />Not affected by worldStop. |

For DBFZ, OnIdling is called even for assist characters that are off-screen.