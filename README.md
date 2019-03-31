# What is this?
This shows newline (technically end-of-line) characters, similar to how Atom or Notepad++ do.

# I just updated to V1, what's different?
- The "returnCharacter" and "crlfCharacter" settings were accidently (originally) switched, V1 corrects that mistake but it might make your endings look different.
- The default color is now the color of your theme whitespace!
- The default line ending for "newlineCharacter" was changed to "¬"
- Toggle line endings by toggling whitespace! (Enabled by default, but can be disabled)
- Set your prefered line ending with "code-eol.validLineEnding", this will color non-valid as errors
- Ending-specific styles. For example use "code-eol.newlineCharacterStyle" to set the color, opacity, etc (see "ThemableDecorationAttachmentRenderOptions" on https://goo.gl/SYzyg8) for individual endings

# What can I customize? (Settings)
You can customize the color, opacity, and which character is used for each kind of end-of-line.<br>
NOTE: after changing a setting, reload vs code for them to take effect. (This is done for performance reasons, but will hopefully will be changed in the future)<br>
Settings Example:
```
        "code-eol.style" {
            "color" : "#2a3f47",
            "opacity" : 1.0
            // there are more settings that can go in here
            // see "ThemableDecorationAttachmentRenderOptions" on https://goo.gl/SYzyg8
        },
        // "code-eol.validLineEnding": "LF"  , // (optional) this makes "CRLF" endings render as error-color
        // "code-eol.validLineEnding": "CRLF", // (optional) this makes "LF" endings render as error-color
        "code-eol.newlineCharacter":"¬",
        "code-eol.returnCharacter" :"⇠",
        "code-eol.crlfCharacter"   :"↵",
        "code-eol.newlineCharacterStyle" : {
            color: "#2a3f47",
            opacity: 0.9
        },
        "code-eol.returnCharacterStyle" : {
            color: "#2a3f47",
            opacity: 0.9
        },
        "code-eol.crlfCharacterStyle" : {
            color: "#2a3f47",
            opacity: 0.9
        },
        // some other symbols you might want to use:
            // ↓
            // ←
            // ↙
            // ⇣
            // ⇠
            // ⇓
            // ⇐
            // ▼
            // ◀
            // ␤
            // ¶
            // ↲
            // ↩
            // ↴
            // ⬎
            // ⇂
        // see more at https://unicode-table.com/en/sets/arrows-symbols/
```
<!-- <img width="376" src="https://github.com/jeff-hykin/code-eol/blob/master/Screen Shot 2018-05-07 at 11.41.35 PM.png"> -->

# Can I toggle line endings with a keybinding?
Yes! There is no default keybinding, but there is a "Toggle (Show/Hide) Line Endings" command that you can use from the command pallet, and you can add a keybinding that maps to it.

# You programmed this yourself?
Nope, the only reason this exists is because its updated/improved fork of https://github.com/sohamkamani/code-eol
The majority of the credit should go to them, I added all the customizations, but I couldn't have done the core myself.

# What does this fork improve?
This fork:
1. Fixes the character bounce issue when typing at the end of a line
2. Lets you customize color and character choice
3. Improves performance
4. Adds more comments/documentation
5. Adds toggle command for turning visible line endings on/off

# What if there is a problem with the extension?
Then post a bug/feature request!<br>
(to do that just create an issue on github: https://github.com/jeff-hykin/code-eol)<br>
The opacity setting, character-specific styles, and the toggle command were created because people on GitHub asked.<br>
NOTE: It might take me awhile to repond on GitHub (I only maintain this in my free time), but I will respond.