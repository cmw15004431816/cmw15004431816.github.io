# Basic writing and formatting syntax

Create a sophisticated formatting for your prose and code on GitHub with simple syntax.

## Headings

To create a heading, add one to six `#` symbols before your heading text. The number of `#` you use will determine the hierarchy level and typeface size of the heading.

```
# A first-level heading
## A second-level heading
### A third-level heading
#### A fourth-level heading
##### A fifth-level heading
###### A sixth-level heading
```

# A first-level heading

## A second-level heading

### A third-level heading

#### A fourth-level heading

##### A fifth-level heading

###### A sixth-level heading

plain text

## Styling text

You can indicate emphasis with bold, italic, strikethrough, subscript or superscript text in comment fields and `.md` files.

Style | Syntax | Keyboard shortcut | Example | Output

Bold | `** **` or `__ __` | `Command`+`B` (Mac) or `Ctrl`+`B` (Windows/Linux) | `**This is bold text**` | __This is bold text__

Italic | `* *` or `_ _` | `Command`+`I` (Mac) or `Ctrl`+`I` (Windows/Linux) | `_This text is italicized_` | *This text is italicized*

Strikethrough | `~~ ~~` | None | `~~This was mistaken text` | ~~This was mistaken text~~

Bold and nested italic | `** **` and `_ _` | None `**This text is _extremely_ important**` | __This text is *extremely* important__

All bold and italic | `*** ***` | None | `***All this text is important***` | _**All this text is important**_

Subscript | `<sub> </sub>` | None | `This is a <sub>subscipt</sub> text` | This is a<sub>subscript</sub> text

Superscript | `<sup> </sup>` | None | `This is a <sup>superscript</sup> text` | This is a<sup>superscript</sup> text

## Quoting text

You can quote text with a `>`.

```
Text that is not a quote

> Text that is a quote
```

Quoted text is indented, with a different type color.

Text that is not a quote

> Text that is a quote

> This is a multi-line quote
>
> Second line

> Text that is a quote
>
> This is a multi-line quote
>
> Second line

>__The text with the quote will be formatted__

## Quoting code

You can call out code or a command within a sentence with single backticks. **The text within the backticks will not be formatted.** You can also press the `Command`+`E` (Mac) or `Ctrl`+`E` (Windows/Linux) keyboard shortcut to insert the backticks for a code block within a line of Markdown.

```
Use `git status` to list all new or modified files that haven't yet been committed.
```

Use `git status` to list all new or modified files that haven't yet been committed.

To format code or text into its own distinct block, use triple backticks.

> Some basic Git commands are:
>
> \`\`\`
>
> git status
>
> git add
>
> git commit
>
> \`\`\`

__Some basic Git commands are:__

```bash
git status
git add
git commit
```

## Supported color models

In issues, pull requests and discussions, you can call out colors within a sentence by using backticks. A supported color model within backticks will display a visualization of the color.

```
The background color is `#ffffff` for light mode and `#000000` for dark mode.
```

The background color is `#ffffff` for light mode and `#000000` for dark mode.

Here are the currently supported color models.

Color | Syntax | Example | Output

HEX | \`#RRGGBB\` | \`#0969DA\` | `#0969DA`

RGB | \`rgb(R,G,B)\` | \`rgb(9, 105, 218)\` | `rgb(9, 105, 218)`

HSL | \`hsl(H,S,L)\` | \`hsl(212, 92%, 45%)\` | `hsl(212, 92%, 45%)`

> ### Note:
> 
> - A supported color model cannot have any leading or trailing spaces within the backticks.
> 
> - The visualization of the color supported in issues, pull requests, and discussions.

## Links

You can create an inline link by warpping link in brackets `[ ]`, and the wrapping the URL in parentheses `( )`. You can also use the keyboard shortcut `Command`+`K` to create a link. When you have text selected, you can paste a URL from your clipboard to automatically create a link from the selection.

You can also create Markdown hyperlink by highlighting the text and using the keyboard shortcut `Command`+`V`. If you'd like to replace the text with the link, use the shortcut `Command`+`Shift`+`V`.

`This site was built using [GitHub Pages](https://pages.github.com/).`

This site was built using [GitHub Pages](https://pages.github.com/).

## Section links

You can link directly to a section in a rendered file by hovering over the section heading to expose :link:.

## Relative links

You can define relative links and image paths in your rendered files to help readers navigate to other files in your repository.

A relative link is a link that is relative to the current file. For example, if you have a README file in root of your repository, and you have another file in *docs/CONTRIBUTING.md*, the relative link to *CONTRIBUTING.md* in your README might look like this:

`[Contribution guidelines for this project](docs/CONTRIBUTING.md)`

GitHub will automatically transform your relative link or image path based on whatever branch you're currently on, so that the link or path always works. The path of the link will be relative to the current file. Links starting with `/` will be relative to the repository root. You can use all relative link operands, such as `./` and `../`.

Your link text should be on a single line. The example below will not work.

```
[Contribution 
guidelines for this project](docs/CONTRIBUTING.md)
```

Relative links are easier for users who clone your repository. Absolute links may not work in clones of your repository - we recommend using relative links to refer to other files within your repository.

## Images

To be continued...

Last updated 07/02/2024
