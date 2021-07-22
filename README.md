# BBEdit Editor Actions

This is a collection of scripts for BBEdit I've found in various places on the web or, occasionally, wrote on my own. These simply add some useful features you might find yourself missing from other editors.

The original version of this package contains some scripts which have been superseded by BBEdit itself, and other scripts which I've removed because I realized I never personally used them. (These are mostly from Oliver Taylor's "Better Tongs" package, linked below if you really want to dive in yourself.)

**Cycle Text Wrap**: Cycles between soft wrap to page guide, soft wrap to window width, and no wrap. (Suggested shortcut: Control-Command-T.)

**Set Tab Width**: brings up a dialog box letting you enter the tab width. (Suggested shortcut: Shift-Command-T. Note that this can, however, be set in the text options menu.)

**Smart Home Move** and **Smart Home Select**: These should be given shortcuts of Command-Left and Shift-Command-Left, respectively; they change the operation of those keys to move or select to the first _non-blank_ character on the left side on first press, and all the way to the first column on the second press. BBEdit lets you set the Home key to work this way, but this is good for those of us who want to leave the Home and End keys working in traditional Mac fashion.

**Join Line with Next**: Does what it says on the tin. (Suggested shortcut: Control-J or Control-Shift-J.)

**Select Inside**: A variation of the balance command which can select text inside quote marks, parentheses, etc. (Suggested shortcut: Control-B or Control-Command-B.)

**Smart New Line**: A complicated one that always creates a new line, but does different things based on the context of the current line:

- If the line ends with `{`, it fills in the closing brace and indents correctly between the two.
- If the line ends with `(` or `({`, it fills in the appropriate close with a semicolon at the end and indents correctly between the two.
- If the line ends with a `:`, it indents the following line. Appropriate for Python.
- If the line is `/**`, it creates a three-line PHP/JavaDoc-style "docblock".
- If the line begins with a bullet character (`-`, `+`, `*`), it continues the bullet on the next line with appropriate indentation. (This also continues docblocks.)
- If the line begins with a number and a period, e.g., `1.`, it continues it with the next number.
- If the line is an HTML list item, it creates another one with the cursor between `<li>` and `</li>` tags, copying any attributes in the current tag to the next one.

Note that the Smart New Line function predates BBEdit's ability to insert matching pairs (e.g., `{}`, `()`, etc.), so if you have insert matching pairs turned on and trigger Smart New Line in a context where it _also_ inserts matching pairs, it will happily duplicate closing braces and parentheses all over the place.

The sources for original versions of these scripts that are still online as of July 2021:

* http://www.angelwatt.com/words/2011/04/11/bbedit-smart-newline-open-line/
* http://www.angelwatt.com/words/2010/07/31/bbedit-textwrangler-home-key-behavior/
* https://github.com/olivertaylor/BetterTongs.bbpackage

The Join Line with Next script originally came from Dennis Rande.
