#Marketplace Style Guide - Copy

##Buttons & Controls
There are 4 types of buttons sizes: `tiny` (24px high), `small` (36px high), `medium` (48px high), and `large` (60px high). Each size has a specific use: `tiny` is used for the purchase button on mobile devices. 'small' is used for I DUNNO. NEEDED? `medium` is used for pretty much everything on tablet and desktop. `large` is reserved for CTAs or marketing purposes.

While buttons have an explicit height, they can vary in width. The ideal width of a button is 10px of padding to the left and right of the button's copy.

Buttons have a 2px drop shadow. The shadow color is the dark secondary of the button's main color.

Unless it is one of the buttons mentioned above, all controls are "action blue".

Some buttons use icons instead of or with text for simplicity/clarity. The same spacing rules mentioned above apply: 10px of padding.


##Input Fields
There are four states for input fields: `normal`, `active`, `error`, and `disabled`.

Text labels are to the left of the input field, unless viewed in mobile portrait. Then the label is placed above the field, aligned left.

Input fields with icons and text use the same 10px padding rules as buttons with icons and text.


##Palettes
There are three palettes: Action, greyscale, and user collection. Each of those have two secondary palettes: light (for highlights, hover) and dark (for shadows, tapped/down states).

Action is used for buttons, alerts, etc. Light blue is for univeral actions: Sign in/sign up, log out, etc. Blue is for positive or benign interactions: Purchase, contact, etc. Green is for success, red means failure or error. Yellow isn't currently used, but could be brought in for queueing or other "wait" actions.

Greyscale is our supporting palette.

The user collection palette is for, you guessed it, collections. But instead of light/dark palettes, the supporting tones are opacity levels: 80%, 60%, 40%. This is to achieve the layered monotone effect used in user collections.


##Typography
The typeface we use for all of our sites is Fira Sans OT. `h1` and `h2` are used on desktop and tablet only. Any code snippets on the dev hub are displayed in Fira Mono OT.


##Grid
We use a responsive frameless grid system for all of our sites. It scales nicely from 4 columns for mobile (320px) to 8 for tablet (640px) to 16 for desktop (1280px). Columns are 60px wide with a 20 px gutter (with 10px padding on either side).
