# Melvor Keybindings
Adds keybindings and remapping functionality to Melvor Idle. View and remap any bindings via the Settings menu (X).

## Installation
[Get the userscript](https://greasyfork.org/en/scripts/434472-keybindings)

## Usage
Simply reference the table below (or that in the Settings menu) and press a key to perform its function.

## List of Default Keybindings
| Function                   | Keybinding                                      |
| -------------------------- | ----------------------------------------------- |
| Menu                       | <kbd>M</kbd>                                    |
| Save                       | <kbd>CTRL</kbd> + <kbd>S</kbd>                  |
| Reload / Character Select  | <kbd>F5</kbd>                                   |
| Open Wiki                  | <kbd>F1</kbd>                                   |
| Settings                   | <kbd>X</kbd>                                    |
| Shop                       | <kbd>V</kbd>                                    |
| Bank                       | <kbd>B</kbd>                                    |
| Combat                     | <kbd>C</kbd>                                    |
| Eat Equipped Food          | <kbd>H</kbd>                                    |
| Loot All (Combat)          | <kbd>SPACE</kbd>                                |
| Run (Combat)               | <kbd>CTRL</kbd> + <kbd>SPACE</kbd>              |
| Equipment Set 1            | <kbd>CTRL</kbd> + <kbd>1</kbd>                  |
| Equipment Set 2            | <kbd>CTRL</kbd> + <kbd>2</kbd>                  |
| Equipment Set 3            | <kbd>CTRL</kbd> + <kbd>3</kbd>                  |
| Equipment Set 4            | <kbd>CTRL</kbd> + <kbd>4</kbd>                  |
| Search Bank                | <kbd>CTRL</kbd> + <kbd>F</kbd>                  |
| Summoning Synergies Menu   | <kbd>S</kbd>                                    |
| Search Summoning Synergies | <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>F</kbd> |
| Woodcutting                | <kbd>1</kbd>                                    |
| Fishing                    | <kbd>2</kbd>                                    |
| Firemaking                 | <kbd>3</kbd>                                    |
| Cooking                    | <kbd>4</kbd>                                    |
| Mining                     | <kbd>5</kbd>                                    |
| Smithing                   | <kbd>6</kbd>                                    |
| Thieving                   | <kbd>7</kbd>                                    |
| Farming                    | <kbd>8</kbd>                                    |
| Fletching                  | <kbd>9</kbd>                                    |
| Crafting                   | <kbd>0</kbd>                                    |
| Runecrafting               | <kbd>!</kbd>                                    |
| Herblore                   | <kbd>@</kbd>                                    |
| Agility                    | <kbd>#</kbd>                                    |
| Summoning                  | <kbd>$</kbd>                                    |
| Astrology                  | <kbd>%</kbd>                                    |
| Alt. Magic                 | <kbd>ALT</kbd> + <kbd>M</kbd>                   |
| Completion Log             | <kbd>Y</kbd>                                    |
| Statistics                 | <kbd>F2</kbd>                                   |
| Golbin Raid                | <kbd>G</kbd>                                    |
| Previous Page              | <kbd>BACKSPACE</kbd>                            |

## API
If you'd like to create a keybinding in your own code managed by Melvor Keybindings, there is a simple API for doing so: `window.kb.register(name, category, defaultKeys, callback)`

```js
// Press 'L' to add oak logs to your bank
if (window.kb)
  window.kb.register(
    'Add oak logs to bank',
    'Cheats',
    { key: 'L', ctrlKey: false, altKey: false },
    () => window.addItemToBank(CONSTANTS.item.Oak_Logs, 100)
  );
```

*Note that `category` is currently unused but planned for implementation as tabs in the future. If your mod has multiple keybindings it might be best to choose your own category now.*

It's also important to note that all keys are in uppercase (e.g., `BACKSPACE` or `ENTER`).
