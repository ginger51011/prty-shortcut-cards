# prty-shortcut cards - Simply pretty Anki cards for keyboard shortcuts

`prty-shortcut` allows for quickly creating nice looking Anki cards for memorizing keyboard
shortcuts for different software.

`prty-shortcut` formats shortcuts automatically, so by entering `Ctrl O` and `M`, `prty-shortcut` will insert
the format below!

## Installation

### Using demo deck

By installing the demo deck containing a few useful Firefox shortcuts, Anki will automatically
import the `prty-shortcut` note type. Simply download [this file](./demo/prty_shortcut_cards_firefox_demo.apkg)
and press <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>I</kbd> in Anki, import the file and _voilà_! The
new card type will become available!

### Manually add the note type

The note type can be also be manually created!

1. Create a new note type (<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>N</kbd> -> `Add`)
2. Select the new note type and click `Fields`
3. Make sure the note has the _exact_ following fields: `Software`, `Action`, `Shortcut Combination` and `Extra Shortcut Combination`. If you want to rename these, you have to change the front and back of the card.
4. Save when done and now press `Cards`
5. Copy [src/front.html](./src/front.html) into `Front Template`, [src/back.html](./src/back.html) into `Back Template` and [src/styles.css](./src/style.css) into `Styles` and save
6. Done! You should now be able to create new notes of the `prty-shortcut` type!

## Usage

I would recommend playing around with the notes to figure it out, but in essence `prty-shortcut` will automatically
assume the formatting of your card. So, by entering _"Ctrl Shift P"_ in `Shortcut Combination`, the card will be generated
as "_<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>"_. The plusses inserted by `prty-shortcut` means that these buttons are to be pressed simultaneously.

Some advanced shortcuts require two separate combinations. This is provided by `Extra Shortcut Combination`, and will 
be formatted as `Shotcut Combination`. This field is not required, and will be ignored if empty.

### Using dark cards without night mode

It is possible to change the CSS (styling, i.e. [this file](/src/style.css)) of the notes so that the dark cards can be
used without night mode. To do this, simple edit the card in Anki:

<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>N</kbd>, select `prty-shortcut` and click `Cards`), go to the `Styling` section and swap place of the following lines:

```css
.card {
```

and

```css
.card.nightMode {
```

Now you will have inversed it all! If you never want the light cards, simple remove everything related to
`.card` , and remove `.nightMode` from the line containing `.card.nightMode`.