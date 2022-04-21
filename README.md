# prty-shortcut cards - Simply pretty Anki cards for keyboard shortcuts

`prty-shortcut` allows for quickly creating nice looking Anki cards for memorizing keyboard
shortcuts for different software.

`prty-shortcut` formats shortcuts automatically, so by entering `Ctrl O` and `M`, `prty-shortcut` will insert
the format below!

## Installation

### Using demo deck

### Manually add the note type
## Usage

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