This is a quick reference guide for Obsidian. 
This version you can copy and paste directly into your Obsidian Vault for quick access.
Just this note, no need for anything else in the repo.

>[!info]+ Legal
>![Creative Commons CC-BY-SA logo|100](https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-sa.png)
>(c) 2026 by [CraftierBark8 on GitHub](https://github.com/CraftierBark8).
>Licensed under [Creative Commons Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/deed.en).
>ver 1.0

>[!failure]- Editing Outside Obsidian
>Obsidian has it's own flavour of markdown with custom extensions and ways of doing things.
>Editing this file in anything but Obsidian will almost definitely lead to the file breaking

>[!warning]- Viewing outside Obsidian
>Obsidian has it's own flavour of markdown that often breaks when viewed in anything except Obsidian.

>[!warning]+ Viewing Mode
>Some things in Obsidian only render while in 'Reading View'. To enter 'Reading View' select the 3 dots icon in the top right of this note and select 'Reading View'. If there's already a checkmark next to it, it's already active.
# Table of Contents

-  [[#-Basic Markdown-|Basic Markdown]]
	- [[#Text Formatting Basics]]
	- [[#Headings]]
	- [[#Lists]]
		- [[#Nested Lists]]
	- [[#Horizontal Lines]]
	- [[#Task Lists & Checkboxes]]
	- [[#Tags]]
- [[#-Advanced Formatting-|Advanced Formatting]]
	- [[#Links]]
		- [[#External Links]]
			- [[#URL Links]]
			- [[#External Images]]
		- [[#Internal Links]]
			- [[#Wikilinks (note links)]]
			- [[#Images and Other Files]]
	- [[#Embeds & Attachments]]
		- [[#Supported File Formats]]
		- [[#PDF Embeds]]
	- [[#Tables]]
	- [[#Callouts]]
		- [[#Collapsible Callouts]]
		- [[#Callout Types]]
	- [[#Code Blocks]]
	- [[#Footnotes]]
	- [[#Comments]]

***
# -Basic Markdown-
***
## Text Formatting Basics
|     Effect     | What to type | What it shows up as |
| :------------: | :----------: | :-----------------: |
|     Normal     |    `text`    |        text         |
|      Bold      |  `**text**`  |      **text**       |
|    Italics     |   `*text*`   |       *text*        |
| Bold & Italics | `***text***` |     ***text***      |
| Strikethrough  |  `~~text~~`  |      ~~text~~       |
|   Highlight    |  `==text==`  |      ==text==       |

You can also nest formatting.
`**This text is bold with *nested italics***.`
**This text is bold with *nested italics***.

To stop markdown from formatting, just put a `\` in front of every formatting mark you don't want used.
`\*\*This will not be bold\*\*`
\*\*This will not be bold\*\*
***
## Headings
Headings are denoted by adding a `#` at the beginning of the new heading. Obsidian supports 6 levels of headings.
```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
***
## Lists
Markdown has 2 different list types, unordered and ordered.

For unordered lists, put a `-` at the beginning of each line you want in the list. You can also use `*` or `+`.
```
- Item 1
- Item 2
- Item 3
```
- Item 1
- Item 2
- Item 3

For ordered lists, do the same but use a number followed by a `.` instead.
```
1. Item 1
2. Item 2
3. Item 3
```
1. Item 1
2. Item 2
3. Item 3
### Nested Lists
For nested lists, just insert a `Tab` (the space, not the word) in front of the ordered or unordered list. You can even mix and match.
```
- Item 1
- Item 2
	1. Item 1-1
	2. Item 1-2
- Item 3
```
- Item 1
- Item 2
	1. Item 1-1
	2. Item 1-2
- Item 3
***
## Horizontal Lines
To insert a horizontal line, just put 3 asterisks on a new line by itself.
```
***
```
***
## Task Lists & Checkboxes
Task lists and checkboxes start as an ordered or unordered list. Just add `[ ]` after the start of the line for an empty checkbox or a `[x]` for a completed checkbox

```
- [ ] Item 1
- [x] Item 2
1. [ ] Item 3
2. [x] Item 4
```
- [ ] Item 1
- [x] Item 2
1. [ ] Item 3
2. [x] Item 4
***
## Tags
Tags allow you to search and organize your Obsidian notes. To add a tag, just put a `#` in front of the tag you want with no space. You can add multiple tags.

```
#QuickReferenceGuide
```
#QuickReferenceGuide
***
# -Advanced Formatting-
***
## Links
Obsidian has 2 types of links, [[#Internal Links]] and [[#External Links]]. Internal links direct you to some file or section of a file within your computer whereas external links go to the internet.

### External Links
External links are links to items online.
#### URL Links
>[!warning]- Links Containing Spaces
>The URL portion of a URL link cannot contain spaces. For example, the following will not work.
>```
>[Example.org](https://www.example.org/no space)
>```
>To get it working, replace all spaces with `%20`. So the example would become:
>```
>[Example.org](https://www.example.org/no%20space)
>```

Probably the simplest type of link. Wrap the text you want to be clickable in brackets (ex. `[text]`) and then right after the `]` wrap your link in `()`. Don't put a space between the sets of brackets.
```
[Example.org](https://www.example.org)
```
[Example.org](https://www.example.org)
#### External Images
>[!warning]- Supported File Formats
>Obsidian only supports certain file formats and your device must have the codecs to display them.
>For an up-to-date list visit [Obsidian Documentation](https://obsidian.md/help/file-formats)
>For a potentially older but offline list in this note, see [[#Supported File Formats]]

To have a link to an embedded image instead of being clickable, just put a `!` before the `[` in the link and make sure the link is to the image specifically. The text wrapped in `[]` should be used as a quick descriptor in case the image cannot load or is broken.

```
![Snowy Mountaintop](https://yavuzceliker.github.io/sample-images/image-1021.jpg)
```
![Snowy Mountaintop](https://yavuzceliker.github.io/sample-images/image-1021.jpg)

To shrink an image to a particular size we can specify the exact number of pixels in width and height. 
To specify, just add `|WIDTHxHEIGHT` before the `]`. Replace `WIDTH` with the width and `HEIGHT` with the height.

```
![Snowy Mountaintop|640x480](https://yavuzceliker.github.io/sample-images/image-1021.jpg)
```
![Snowy Mountaintop|640x480](https://yavuzceliker.github.io/sample-images/image-1021.jpg)

To scale with the original aspect ratio, just put the width (ex. `|640`) and the height will scale accordingly.

```
![Snowy Mountaintop|640](https://yavuzceliker.github.io/sample-images/image-1021.jpg)
```
![Snowy Mountaintop|640](https://yavuzceliker.github.io/sample-images/image-1021.jpg)
### Internal Links
Internal links can link to files, images, markdown notes and even sections of markdown notes.
#### Wikilinks (note links)
Wikilinks are quick links to notes and sections of notes in the same Obsidian Vault.
By default, Obsidian uses Wikilinks instead of traditional markdown links. We will only cover the Obsidian way here.
>[!tip]- Change Default Behaviour of Wikilinks
>If you want to, you can change Obsidian to use standard markdown links instead of Wikilinks.
>Go to Settings > Files & Links > Use \[\[Wikilinks\]\] and toggle it to off.

To use Wikilinks, just put the name of the note you want to reference in `[[]]`. Obsidian will even display a list of notes you can link to when you use `[[]]`.
```
[[Obsidian Quick Reference]]
```
[[Obsidian Quick Reference]]

You can make links to a specific Heading within a note, just add a `#` after the note name and put the heading name.
```
[[Obsidian Quick Reference#Wikilinks (note links)]]
```
[[Obsidian Quick Reference#Wikilinks (note links)]]

>[!info]+ Number of `#`
>Only put one `#` no matter the number of `#` you put for that heading in the note.

If you are referencing the note you are currently in, you can simplify the link by just including the heading portion.
```
[[#Wikilinks (note links)]]
```
[[#Wikilinks (note links)]]

To put display text instead of the full link, put `|Display Text` at the end of the link.
```
[[Obsidian Quick Reference#Wikilinks (note links)|Link to Wikilinks Section]]
```
[[#Wikilinks (note links)|Link to Wikilinks Section]]

#### Images and Other Files
You can also make internal links to any file in your vault. It's the same as a Wikilink except put the name of the file with the file extension. Supported file types will open in Obsidian. See [[#Supported File Formats]] for more info. 

I will make a link to a PDF as an example.[^1]
```
[[Obsidian Quick Reference Example PDF.pdf]]
```
***
## Embeds & Attachments
Embeds allow you link to content somewhere else
>[!note]- Embedding an External Image
>If you're looking to embed an external image, that info can be found in [[#External Images]]

>[!note]+ How to Make Links
>For information on how to make links that you can embed, see [[#Links]].
>

You can embed many things in Obsidian by simply adding a `!` in front of the item's link. For example, I want to embed my example note.[^1]
```
![[Example Note]]
```
### Supported File Formats
For an up-to-date list of all supported embeds and attachments, go to [Obsidian's Documentation on Supported Files](https://obsidian.md/help/file-formats).
>[!warning]- Audio and Video Codecs
>Although Obsidian may support a file format, your device must have the necessary codecs and support installed to display or play them.

As of writing, Obsidian supports:
- Markdown: `.md`
- Bases: `.base`
- JSON Canvas: `.canvas` ([Learn More](https://jsoncanvas.org/))
- Images: `.avif`, `.bmp`, `.gif`, `.jpeg`, `.jpg`, `.png`, `.svg`, `.webp`
- Audio: `.flac`, `.m4a`, `.mp3`, `.ogg`, `.wav`, `.webm`, `.3gp`
- Video: `.mkv`, `.mov`, `.mp4`, `.ogv`, `.webm`
- PDF: `.pdf`
>[!info]- Adding More File Formats
>The formats Obsidian supports can be expanded with [Community Plugins](https://obsidian.md/help/community-plugins)

For an easier way of adding attachments, simply drag and drop them into the note and they will automatically be added to your vault. You can also copy and paste them.
### PDF Embeds
PDFs have additional formatting options in Obsidian.

A standard embed link looks like this.[^1]
```
![[Example.pdf]]
```

To specify a page to display, you can add `#page=N` after the name of the PDF, where N is the page number.[^1]
```
![[Example.pdf#page=1]]
```

You can also specify the height of the PDF by adding `#height=N` to the link, where N is the height you want displayed in pixels.[^1]
```
![[Example.pdf#page=2]]
```
***
## Tables
>[!warning]- Tables Created in Text
>Tables created by the user typing them out will not render as tables unless in 'Reading View' mode. To avoid this issue and for much easier table creation, right click where you want a table, select `Insert` then `Table`.

>[!tip]+ Formatting in Tables
>You can include embeds, links, text formatting and almost anything else you can do outside a table, within a table in Obsidian.

Use `|` and `-` to create tables in text and Obsidian will render them into nice looking tables.
```
| Heading 1 | Heading 2 |
|-----------|-----------|
| A         | B         |
```
| Heading 1 | Heading 2 |
|-----------|-----------|
| A         | B         |


Although Obsidian defaults alignment to the left, you can customize that per column by inserting a `:` in the right place as shown below.
```
| Left | Center | Right |
|:-----|:------:|------:|
| A    | B      | C     |
```
| Left | Center | Right |
|:-----|:------:|------:|
| A    | B      | C     |

Not all those `|` and `-` are actually necessary to render a table, people write them like that so they look nice and readable in text form. You can write a more minimal table like below.
```
Left | Center | Right
---|:-:|--:
A | B | C
```
Left | Center | Right
---|:-:|--:
A | B | C
***
## Callouts
Callouts are great ways to get you or your reader's attention with notes, warnings, tips, etc. 
To start a callout, on a new line put `>[!TYPE]` with `TYPE` replaced with the callout type. 

To add content to a callout just put a new line with a `>`.
```
>[!note]
>This is example text!
```
>[!note]
>This is example text!!

By default, callouts use the callout type as the title but you can actually add your own. Just put a space after the `]` and put the title.

```
>[!note] I'm an example
```
>[!note] I'm an example
### Collapsible Callouts
To make a callout collapsible, just add a `+` or `-` just after the `]`.
`-` is for callouts which start collapsed and `+` is for callouts that start expanded.
Just click to expand or collapse.

```
>[!note]- I'm an example
>And this is example text.
```
>[!note]- I'm an example
>And this is example text.
### Callout Types
Listed below is every callout type.

`>[!note]`
>[!note]

`>[!abstract]` -  also called `summary` and `tldr`
>[!abstract]

`>[!info]`
>[!info]

`>[!todo]`
>[!todo]

`>[!tip]` - also called `hint` and `important`
>[!tip]

`>[!success]` - also called `check` and `done`
>[!success]

`>[!question]` - also called `help` and `faq`
>[!question]

`>[!warning]` - also called `question` and `attention`
>[!warning]

`>[!failure]` - also called `fail` and `missing`
>[!failure]

`>[!danger]` - also called `error`
>[!danger]

`>[!bug]`
>[!bug]

`>[!example]`
>[!example]

`>[!quote]` - also called `cite`
>[!quote]

***
## Code Blocks
There are 2 types of code blocks. Regular code blocks and in-line code. Formatting does not get applied within code blocks or in-line code.
For information on how to make in-line code, see [[#Text Formatting Basics]].

Code blocks are created by making a line of \`\`\` (3 back quotes) in a row on it's own line.
And then make a 2nd line of \`\`\` in a row on it's own. Most of the time Obsidian will do the 2nd line for you. Any line in between the 2 lines of back quotes will be the code block.
```
This is a code block
```

To specify the language of the code block, add the language name after the first line of \`\`\`
```python
print("This is some python code")
```
***
## Footnotes
Footnotes are great ways of including citations or notes that don't need a callout.

To add a footnote to some text, put `[^N]` where N is the footnote number. Obsidian will start suggesting existing footnotes after the `^`
```
This is an example.[^2]
```
This is an example.[^2]

Footnote definitions should be at the end of the document but you can put them anywhere in editing mode[^3]. To start a footnote definition, make a new line and put `[^N]:` where N is the footnote number. Make sure you leave a space after the `:`.
```
[^2]: This is also an example
```
[^2]: This is also an example
***
## Comments
Comments don't show up in reading view, only editing mode. Making them useful for hidden text or information you only need while editing.

Comments are very similar to code blocks except they use `%%` (2 percentage symbols) in a row instead.
>[!info]- Display Example
>The display example (the one outside the code block) can only be viewed in editing mode.
```
%%
This is an example comment
%%
```
%%
This is an example comment
%%
***
## QRG Footnotes
Footnotes for this Quick Reference Guide.

[^1]: Actually displaying this item would require an additional item in the vault. Since I want this to be a single note, a display example is unavailable, only the text version (in code block).
[^2]: This is also an example
[^3]: Footnote definitions get moved to the bottom of the note and properly ordered when in reading mode.