# Markdown

Markdown is a simple [markup language](https://en.wikipedia.org/wiki/Markup_language). Markup languages are used to give computer programs directions on how particular blocks of text should be processed. Markdown was developed in 2004 by writer and developer [John Gruber](http://daringfireball.net). Gruber describes Markdown on his [website](http://daringfireball.net/projects/markdown/):

> Markdown is intended to be as easy-to-read and easy-to-write as is feasible.

> Readability, however, is emphasized above all else. A Markdown-formatted document should be publishable as-is, as plain text, without looking like it’s been marked up with tags or formatting instructions. While Markdown’s syntax has been influenced by several existing text-to-HTML filters — including Setext, atx, Textile, reStructuredText, Grutatext, and EtText — the single biggest source of inspiration for Markdown’s syntax is the format of plain text email.

> To this end, Markdown’s syntax is comprised entirely of punctuation characters, which punctuation characters have been carefully chosen so as to look like what they mean. E.g., asterisks around a word actually look like *emphasis*. Markdown lists look like, well, lists. Even blockquotes look like quoted passages of text, assuming you’ve ever used email...

> ...Markdown’s syntax is intended for one purpose: to be used as a format for writing for the web.

Markdown is utilized to varying degrees by many of the data science tools we'll use in both courses, including RStudio, GitHub, and Slack. In all three applications, Markdown provides a straightforward way to format and stylize plain text files. Markdown therefore gives us the best of two worlds - text files can be organized and formatted as in [WYSIWYG](https://en.wikipedia.org/wiki/WYSIWYG) editors like Microsoft Word, but they remain plain text files that are accessible in a variety of computing environments and do not depend on proprietary applications.

## Document Organization
There are two principle means for organizing Markdown documents - headings of varying size and paragraph breaks.

### Headings
Markdown contains six heading levels. Headings are identified with `#` symbols and a space that separates them from from the heading text.

**Input:**
```markdown
# This is the largest heading
## This is the second largest heading
### This is the third largest heading
#### This is the fourth largest heading
#### This is the second smallest heading
###### This is the smallest heading
```

**Output:**
<img src="images/markdownHead.png" width="50%" style="display: block; margin: auto auto auto 0;" />

### New Paragraphs
Leave a blank line between two paragraphs to create a break.

**Input:**
```markdown
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 
incididunt ut labore et dolore magna aliqua. Quam pellentesque nec nam aliquam 
sem et tortor consequat. Auctor urna nunc id cursus metus. Eleifend mi in 
nulla posuere. Facilisis sed odio morbi quis. Nibh nisl condimentum id venenatis. 
Lectus nulla at volutpat diam ut venenatis. 

Pretium lectus quam id leo in vitae. Neque vitae tempus quam pellentesque nec nam 
aliquam. Curabitur gravida arcu ac tortor. Arcu risus quis varius quam quisque id 
diam. Viverra aliquet eget sit amet tellus cras adipiscing. Tellus molestie nunc 
non blandit massa enim nec. Tempus imperdiet nulla malesuada pellentesque elit eget. 
Non blandit massa enim nec. Sed risus pretium quam vulputate dignissim suspendisse 
in est ante.
```

**Output:**

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Quam pellentesque nec nam aliquam sem et tortor consequat. Auctor urna nunc id cursus metus. Eleifend mi in nulla posuere. Facilisis sed odio morbi quis. Nibh nisl condimentum id venenatis. Lectus nulla at volutpat diam ut venenatis. 

Pretium lectus quam id leo in vitae. Neque vitae tempus quam pellentesque nec nam aliquam. Curabitur gravida arcu ac tortor. Arcu risus quis varius quam quisque id diam. Viverra aliquet eget sit amet tellus cras adipiscing. Tellus molestie nunc non blandit massa enim nec. Tempus imperdiet nulla malesuada pellentesque elit eget. Non blandit massa enim nec. Sed risus pretium quam vulputate dignissim suspendisse in est ante.

## Working with Text
Markdown provides a number of tools for working with and stylizing text. These include options for bold and italicized text, adding code blocks, quoting text, and creating bulleted and enumerated lists.

### Styling Text
Text can be styled using bold and italics To create italicized text, wrap your text with a single asterisk `*`. To create bold text, wrap your text with double asterisks `**`. 

**Input:**
```markdown
*This is an italicized sentence.*

**This is a bolded sentence.**
```

**Output:**

*This is an italicized sentence.*

**This is a bolded sentence.**

### Quoting Text
Quoting text (which I have used above to illustrate examples) is done with a greater then symbol (`>`).

**Input:**
```
> This is quoted text.
```

**Output:**

> This is quoted text.

### Quoting Code
There are two types of code quotes in Markdown. In-line quotes, which are included in a sentence, are wrapped in single backticks:
> Use the `describe` command to list variables in `R`

To include code blocks, which are better for including the full syntax of particular commands and their output, use triple backticks:

```Stata
. describe make price mpg

              storage   display    value
variable name   type    format     label      variable label
--------------------------------------------------------------------------------
make            str18   %-18s                 Make and Model
price           int     %8.0gc                Price
mpg             int     %8.0g                 Mileage (mpg)
```

Note how the word 'Stata' is written after the first set of triple backticks. This is an indicator for GitHub that the code is written in Stata's programming language. By including this, GitHub can apply some syntax highlighting to your files. This makes them easier to read.

### Links
In Markdown, adding hyperlinks is a two step process. The text that you want to have hyperlinked is written first and is wrapped in brackets `[]`. After this, you include the URL wrapped in parentheses `()`. This is an example of including in-line hyperlinks:

> The course [website](https://github.com/slu-soc5050) is hosted using the service [GitHub](https://github.com).

### Embedding Images
Within the directory that contains your Markdown file, create a subdirectory called `Output`. Save all images for a particular assignment there. In your main assignment Markdown file, include a hyperlink reference:



Note how, instead of including text to be hyperlinked, we suppress this aspect of the syntax by using an exclamation point `!`.

### Simple Lists
Bulleted lists are indicated in Markdown using the dash `-` or a single asterisk `*`:

> - mean
> - median
> - mode
> * variance
> * standard deviation

Enumerated lists are created by preceding each line with the appropriate number:

> 1. calculate the mean
> 2. calculate the variance
> 3. calculate the standard deviation

You can create more complex lists by preceding a line with two single spaces. You can also combine bulleted and enumerated lists when using this approach.

## GitHub Markdown
These are specific to what is called GitHub Markdown - there are some subtle differences in the way GitHub uses Markdown formatting.

### Styling Text
Text can be styled using bold, italics, and strikethroughs. To create italicized text, wrap your text with a single asterisk `* *`. To create bold text, wrap your text with double asterisks `** **`. To create strike-through text, wrap your text with two tildes `~~ ~~`.

> ~~This is a sentence with strikethrough text~~

### Tables

### Task Lists
If you want to create task lists on GitHub, you can include brackets separated by a space before each list item `[ ]`. Completed tasks include an `x` in place of the space `[x]`.  These task lists are interactive - when published on GitHub, you can click on the resulting checkboxes to toggle them between complete / incomplete.

> 1. [x] calculate the mean
> 2. [ ] calculate the variance
> 3. [ ] calculate the standard deviation

### Mentioning Other GitHub Users
If you want to mention me or one of your classmates in a comment, include the `@` symbol before their username:

> Hey @chris-prener, thanks for the feedback. I made the changes to lines 40 and 41.

Once the document is uploaded to GitHub, the username will render as a hyperlink and the user will be alerted.