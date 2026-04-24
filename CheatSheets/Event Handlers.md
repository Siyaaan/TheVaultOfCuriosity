

## Example

| **Event**           | **Logic**            | **Data available in event**           | Example                               |
| ------------------- | -------------------- | ------------------------------------- | ------------------------------------- |
| **`onclick`**       | Primary click        | Coordinates, button used (left/right) | onclick: move \|_\|                   |
| **`ondoubleclick`** | Rapid two clicks     | Same as click                         | **`ondoubleclick: move \|_\|`**       |
| **`onmouseenter`**  | Hover begins         | Mouse position                        |                                       |
| **`onmouseleave`**  | Hover ends           | Mouse position                        |                                       |
| **`onmousedown`**   | Button pressed       | Useful for drag-and-drop              |                                       |
| **`onmouseup`**     | Button released      | Useful for drag-and-drop              |                                       |
| **Event**           | **Location**         | **Action Trigger**                    | **Typical Payload (evt.value())**     |
| [[oninput]]         | `input`, `textarea`  | Every single keystroke                | The entire current string in the box. |
| **`onclick`**       | `button`, `a`, `div` | A mouse click/tap                     | Usually ignored (used for actions).   |
| **`onchange`**      | `select`, `checkbox` | When focus leaves or toggle           | The selected option or "true/false".  |
| **`onkeydown`**     | `window`, `input`    | Pressing a specific key               | The name of the key (e.g., "Enter").  |


[[event handlers act as a variable replacement]]