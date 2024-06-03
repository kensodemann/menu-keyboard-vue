# Keyboard Navigation in Sidemenu Apps

## Executed Behavior

The following is the expected "default" behavior for navigation using `Tab` and `Spacebar`.

### With the Split Pane Open

1. Hitting `Tab` cycles through the menu items.
1. Hitting `Spacebar` at any point would select the page for that item. This seems like it should close the menu because of the `ion-menu-toggle`.
1. Hitting `Tab` should cycle through the buttons on the page.
1. Hitting `Spacebar` or `Enter` on any button should trigger a `click` response (in this case an `alert` will be shown).
1. Continuing to hit `Tab` will cycle through the selectable items (URL bar in browser, menu items, buttons).

### With the Split Pane Closed

1. Hitting `Tab` cycles through the buttons including the hamburger menu button.
1. When the hamburger menu item is selected, hitting `Spacebar` should open the menu.
1. So long as an item is _not_ selected, hitting `Tab` should continue cycling through the menu items.
1. Upon hitting `Spacebar` on a menu item, the menu should close and the first button on the page should be focused.
1. Hitting `Tab` at this point should continue the cycle through the buttons including the hamburger menu button.

## Discrepancies

Android testing was performed on a physical Pixel 4 device. Android testing only included Split Pane Closed as the device used is too small for the split pane to be open.

iOS testing was performed on a physical iPad.

Web testing was performed on Chrome.

| Problem                                                                                                                    | Android | iOS | Web | Split Pane Open / Closed |
| -------------------------------------------------------------------------------------------------------------------------- | :-----: | :-: | :-: | :----------------------: |
| Navigation with the `Tab` key skips all of the menu items                                                                  |    X    |  X  |  X  |           Both           |
| Navigation with the `Tab` key navigates to the menu button and allows the opening of the button, but then navigation stops |    X    |  X  |  X  |          Closed          |

Basically, keyboard navigation of the menu does not work.
