# Melvor Keybindings
Adds keybindings and remapping functionality to Melvor Idle. View and remap any bindings via the Settings menu (X).

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
| Alt. Magic                 | <kbd>%</kbd>                                    |
| Milestones                 | <kbd>Y</kbd>                                    |
| Mastery                    | <kbd>U</kbd>                                    |
| Item Log                   | <kbd>I</kbd>                                    |
| Monster Log                | <kbd>O</kbd>                                    |
| Pet Log                    | <kbd>P</kbd>                                    |
| Statistics                 | <kbd>F2</kbd>                                   |
| Golbin Raid                | <kbd>G</kbd>                                    |
| Previous Page              | <kbd>BACKSPACE</kbd>                            |
| Equipment Set 1            | <kbd>CTRL</kbd> + <kbd>1</kbd>                  |
| Equipment Set 2            | <kbd>CTRL</kbd> + <kbd>2</kbd>                  |
| Equipment Set 3            | <kbd>CTRL</kbd> + <kbd>3</kbd>                  |
| Search Bank                | <kbd>CTRL</kbd> + <kbd>F</kbd>                  |
| Summoning Synergies Menu   | <kbd>S</kbd>                                    |
| Search Summoning Synergies | <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>F</kbd> |

## API
If you'd like to create a keybinding in your own code managed by Melvor Keybindings, there is a simple API for doing so: `window.kb.register(name, category, defaultKeys, callback)`

```js
if (window.kb)
  window.kb.register(
    'Add oak logs to bank',
    'General',
    { key: 'L', ctrlKey: false, altKey: false },
    () => window.addItemToBank(CONSTANTS.item.Oak_Logs, 1)
  );
```

*Note that `category` is currently unused but planned for implementation as tabs in the future. If your mod has multiple keybindings it might be best to choose your own category now.*