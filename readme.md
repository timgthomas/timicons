# Timicons

File type icons for Code.

## Dev Requirements

To compile the icons from source, you'll need [`sketchtool`](https://developer.sketch.com/cli/): A CLI from Sketch.

## Adding a new icon

1. Create the icon vector in the Sketch file with an artboard name (e.g. `doc-elixir`)
1. Add a new codepoint in `fantasticonrc.js` (e.g. `'doc-elixir': 0xE031`)
1. Update `extension/timicons-icon-theme.json` with the icon definition, referencing the new codepoint:
   ```json
   "doc.elixir": {
     "fontCharacter": "\uE031"
   }
   ```
1. Add the icon definition to a folder, file extension, or filename
1. Run `npm start` to extract the icon, create a new type file, and update the extension
1. Restart Code to see your changes (new icons aren't automatically loaded)
