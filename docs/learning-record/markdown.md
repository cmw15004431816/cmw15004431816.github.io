# Basic writing and formatting syntax

Create a sophisticated formatting for your prose and code on GitHub with simple syntax.

## Headings

TO create a heading, add one to six `#` symbols before your heading text. The number of `#` you use will determine the hierarchy level and typeface size of the heading.

```
# A first-level heading
## A second-level heading
### A third-level heading
#### A fourth-level heading
##### A fifth-level heading
###### A sixth-level heading
```
![img](../img/1.png)
<!--This is the same as ![img](/docs/img/1.png)-->

## Styling text

You can indicate emphasis with bold, italic, strikethrough, subscript or superscript text in commment fields and `.md` files.

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

You can call out code or a command within a sentence with single baketicks. **The text within the backticks will not be formatted.** You can also press the `Command`+`E` (Mac) or `Ctrl`+`E` (Windows/Linux) keyboard shortcut to insert the backticks for a code block within a line of Markdown.

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

> This feature is only available on GitHub, it will not work on MkDocs

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

GitHub will automatically transform your relative link or image path based on whatever branch you're currently on, so that the link or path always works. The path of the link will be relative to the current file. **Links starting with `/` will be relative to the repository root. You can use all relative link operands, such as `./` and `../`.**

> `/` represents the root of the repository
> 
> `./` represents the current path
>
> `../` represents the parent path of the current path
>
> When there is no link operands ahead, it is the same as the link starting with `./`
> 
> - Example: `docs/CONTRIBUTING.md` is equivalent to `./docs/CONTRIBUTING.md`
> 
> When you are currently at the root of the repository, these three links are equivalent:
> 
> - `docs/CONTRIBUTING.md`(Current is the root)
> - `./docs/CONTRIBUTING.md`(Same as the last one)
> - `/docs/CONTRIBUTING.md`(Root is current)
> 
> In other cases, `docs/CONTRIBUTING.md` and `/docs/CONTRIBUTING.md` point to different paths, they are not equvalent

Your link text should be on a single line. The example below will not work.

```
[Contribution 
guidelines for this project](docs/CONTRIBUTING.md)
```

Relative links are easier for users who clone your repository. Absolute links may not work in clones of your repository - we recommend using relative links to refer to other files within your repository.

## Images

You can display an image by adding `!` and wrapping the alt text in `[ ]`. Alt text is a short text equivalent of the information in the image. Then, wrap the link for the image in parentheses `( )`.

`![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://myoctocat.com/assets/images/base-octocat.svg)`

![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://myoctocat.com/assets/images/base-octocat.svg)

> Note: When you want to display an image that is in your repository, use relative links instead of absolute links.

Here are some examples for using relative links to display an image.

Context | Relative Link

In a `.md` file on the same branch | `/assets/images/electrocat.png`

In a `.md` file on another branch | `/../main/assets/images/electrocat.png`

In issues, pull requests and comments of the repository | `../blob/main/assets/images/electrocat.png?raw=true`

In a `.md` file in another repository | `/../../../../github/docs/blob/main/assets/images/electrocat.png`

In issues, pull requests and comments of another repository | `../../../github/docs/blob/main/assets/images/electrocat.png?raw=true`

> Note: The last two relative links in the table above will work for images in a private repository only if the viewer has at least read access to the private repository that contains these images.

## Specifying the theme an image is shown to

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/25423296/163456776-7f95b81a-f1ed-45f7-b7ab-8fa810d529fa.png">
  <source media="(prefers-color-scheme: light)" srcset="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
  <img alt="Shows an illustrated sun in light mode and a moon with stars in dark mode." src="https://user-images.githubusercontent.com/25423296/163456779-a8556205-d0a5-45e2-ac17-42d089e3c3f8.png">
</picture>

Last updated 07/03/2024
