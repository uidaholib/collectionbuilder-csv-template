# Notes on using Markdown for the About page

## Citations

You'll need to cite the sources for your multimedia essay just as you would for any academic essay.
Whenever possible, use [Turabian Style](https://www.chicagomanualofstyle.org/turabian/turabian-notes-and-bibliography-citation-quick-guide.html){:target="_blank" rel="noopener"} to add your essay citations as footnotes.

To add a footnote in Markdown, directly after the sentence you'd like to cite, add a left square bracket (`[`), followed by a caret symbol (`^`), followed by a footnote number (i.e. `1`, `2`, `3`, etc.), followed by a left square bracket (`]`). See below for an example:

`Example text to be cited.[^1]`

`Yet more text to cite.[^2]`

Then, at the very bottom of the page, you'll create a section with the heading `Sources`, and add the bracketed footnote numbers (i.e. `[^1]`, `[^2]`, `[^3]`, etc.), followed by a colon (`:`) and citation, like this:

`[^1]: Katie Kitamura, *A Separation* (New York: Riverhead Books, 2017), 25.`

`[^2]: Sharon Sassler and Amanda Jayne Miller, *Cohabitation Nation: Gender, Class, and the Remaking of Relationships* (Oakland: University of California Press, 2017), 114.`

On the front end, your footnote number will automatically link down to its corresponding citation, which will reside at the "foot" of your essay.
To see this in action, look at the cited text below, and click on the blue `1` and `2` footnotes at the end of each line.

---

## Hyperlinks

You can create hyperlinks in Markdown like this:

`[GitHub Help](https://help.github.com/)`

You've probably noticed that hyperlinks created this way cause a new website to open in your browser's *current tab*.
Sometimes this is what you want to happen, but there will be other times where you'd like a link to open in a *new browser tab* when a user clicks on it.
To make this happen, you'll need to copy and paste the snippet of text below to the *end* of your hyperlink parentheses:

Copy this: `{:target="_blank" rel="noopener"}`

And paste it *after* the parentheses in your hyperlink: 

`[GitHub Help](https://help.github.com/){:target="_blank" rel="noopener"}`

This will ensure that your link opens in a new tab, like this: [GitHub Help](https://help.github.com/){:target="_blank" rel="noopener"}

---

## Horizontal Line Breaks

Sometimes you may want to add greater distinction between sections of your essay.
You can do this by adding a "horizontal line break," which is a horizontal line that stretches across the width of the page.

Horizontal line breaks are easy to do in Markdown.
Simply add three hyphens in a row to a new line, and make sure the line with the hyphens is preceded and followed by blank lines, like this:

```

---
```

On the front end, a horizontal line break will look like this:

---

## Table of contents

If you break the About page into sections you can title each of those sections using headings.
To do this, use the various heading sizes:

`# Heading 1` should only be used once, for title

`## Heading 2` should be used for sections of your page

`### Heading 3` should be used for sub-sections of your page

You can have multiple headings of the same type throughout your essay, and nest headings hierarchically just as you would an outline, like this: 

```
# First Heading 1

## First Heading 2

### First Heading 3

## Second Heading 2
```

...which looks like this on the front end:

# First Heading 1

## First Heading 2

### First Heading 3

## Second Heading 2

**Remember, always separate a heading from the text below it with a blank line.** 

If you do incorporate headings, you'll probably find it convenient to make use of the table of contents feature at the top of the essay.

The table of contents is generated from the include that looks like this:

`{% raw %}{% include feature/nav-menu.html sections="About CollectionBuilder SA;About the About Page" %}{% endraw %}`

"sections" is followed by an equals sign (`=`) and values separated by semicolons and encased with quotation marks.

The two values inside the quotation marks correspond to headings in the default about.md file:

`## About CollectionBuilder SA`

`## About the About Page`

**In order for the contents box to work correctly, the word in the Table of Contents Include needs to match a heading somewhere in your essay.**
When you click on the links in the table of contents, and your page will automatically scroll down to the corresponding section.