# Intro To Markdown

Markdown is a simple way to format plain text. You write normal text with a few special characters, and a Markdown viewer turns it into nicely formatted output.

Every section below has two parts:

- **Write this:** the Markdown you type
- **Get this:** what it looks like once it is rendered

> **Tip:** In VS Code, press `Ctrl+Shift+V` to open a preview of this file and see the rendered version.

## Table of Contents

1. [Headings](#headings)
2. [Paragraphs and Line Breaks](#paragraphs-and-line-breaks)
3. [Bold and Italics](#bold-and-italics)
4. [Blockquotes](#blockquotes)
5. [Lists](#lists)
6. [Horizontal Rules](#horizontal-rules)
7. [Links](#links)
8. [Images](#images)
9. [Code](#code)
10. [Escaping Characters](#escaping-characters)
11. [Extended Syntax](#extended-syntax)
12. [More Information](#more-information)

---

## Headings

Start a line with one to six `#` symbols. More `#` symbols means a smaller heading.

- Always put a **space** after the `#` symbols, or some Markdown viewers will not recognize the heading.
- Put a blank line before and after each heading.

**Write this:**

```markdown
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

**Get this:**

# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

---

## Paragraphs and Line Breaks

Do **not** indent paragraphs, just start writing. To start a **new paragraph**, leave a blank line between your lines of text.

**Write this:**

```markdown
This is my first paragraph.

This is my second paragraph.
```

**Get this:**

This is my first paragraph.

This is my second paragraph.

If you just press Enter once, Markdown joins the lines back together into one line. To force a **line break** without starting a new paragraph, you have three options:

1. End the line with **two or more spaces** (they are invisible, so be careful!)
2. End the line with a backslash `\`
3. Use the HTML `<br>` tag

**Write this:**

```markdown
This line ends with two spaces  
so I am on a new line.

This line ends with a backslash\
so I am on a new line.

This line uses an HTML tag<br>so I am on a new line.
```

**Get this:**

This line ends with two spaces  
so I am on a new line.

This line ends with a backslash\
so I am on a new line.

This line uses an HTML tag<br>so I am on a new line.

---

## Bold and Italics

Wrap text in asterisks `*` (or underscores `_`) to style it.

**Write this:**

```markdown
This is **bold** text.

This is *italic* text.

This is ***bold and italic*** text.
```

**Get this:**

This is **bold** text.

This is *italic* text.

This is ***bold and italic*** text.

---

## Blockquotes

Start a line with `>` to make a quote. Use `>>` to put a quote inside a quote.

**Write this:**

```markdown
> This is a blockquote.
>
> It can have more than one paragraph.
>
>> This is a quote inside a quote.
```

**Get this:**

> This is a blockquote.
>
> It can have more than one paragraph.
>
>> This is a quote inside a quote.

---

## Lists

### Ordered Lists

Start each line with a number and a period.

**Write this:**

```markdown
1. First item
2. Second item
3. Third item
```

**Get this:**

1. First item
2. Second item
3. Third item

The actual numbers you type do not matter, as long as the list **starts with 1**. Markdown counts for you.

**Write this:**

```markdown
1. First item
1. Second item
1. Third item
2. Fourth item
7. Fifth item
```

**Get this:**

1. First item
1. Second item
1. Third item
2. Fourth item
7. Fifth item

### Unordered Lists

Start each line with `-`, `*`, or `+`. Pick one and stick with it.

**Write this:**

```markdown
- First item
- Second item
- Third item
```

**Get this:**

- First item
- Second item
- Third item

### Nested Lists

Indent an item to put it inside another list.

**Write this:**

```markdown
1. Fruits
   - Apple
   - Banana
2. Vegetables
   - Carrot
   - Broccoli
```

**Get this:**

1. Fruits
   - Apple
   - Banana
2. Vegetables
   - Carrot
   - Broccoli

---

## Horizontal Rules

Put three dashes `---` on a line by themselves to draw a line across the page. Leave a blank line above it, or Markdown may turn the text above into a heading.

**Write this:**

```markdown
Text above the line.

---

Text below the line.
```

**Get this:**

Text above the line.

---

Text below the line.

---

## Links

Put the link text in square brackets `[ ]` and the web address in parentheses `( )`.

**Write this:**

```markdown
Search the web with [Google](https://www.google.com).
```

**Get this:**

Search the web with [Google](https://www.google.com).

### Links to Sections of This Page

You can also link to a heading on the same page. Use `#` followed by the heading text in lowercase, with spaces replaced by dashes. That is how the [Table of Contents](#table-of-contents) at the top works.

**Write this:**

```markdown
Jump back up to the [Lists](#lists) section.
```

**Get this:**

Jump back up to the [Lists](#lists) section.

---

## Images

Images look just like links, but start with an exclamation point `!`. The text in square brackets is the **alt text**, which is shown if the image can't load and is read aloud by screen readers.

**Write this:**

```markdown
![Markdown logo](https://cdn.prod.website-files.com/650b227bcdb8ac34f48bf223/651f64cd1dd245d647d0f222_651f284d8907825f8784fa22_Markdown.jpeg)
```

**Get this:**

![Markdown logo](https://cdn.prod.website-files.com/650b227bcdb8ac34f48bf223/651f64cd1dd245d647d0f222_651f284d8907825f8784fa22_Markdown.jpeg)

---

## Code

### Inline Code

Wrap a small piece of code in single backticks `` ` `` to show it inside a sentence.

**Write this:**

```markdown
Use the `print()` function to show output in Python.
```

**Get this:**

Use the `print()` function to show output in Python.

### Code Blocks

Put three backticks ` ``` ` on the line before and the line after your code. You can add the name of the language right after the first three backticks to get color highlighting.

**Write this:**

````markdown
```python
def my_function(name):
    return f"Hello {name}"
```
````

**Get this:**

```python
def my_function(name):
    return f"Hello {name}"
```

### Indented Code Blocks

You can also make a code block by indenting each line with **four spaces** (or one tab). Leave a blank line before it.

**Write this:**

```markdown
Here is some HTML:

    <a href="https://example.com"><img src="funny-image.png"></a>
```

**Get this:**

Here is some HTML:

    <a href="https://example.com"><img src="funny-image.png"></a>

---

## Escaping Characters

What if you want to show a `*` or `#` without Markdown turning it into formatting? Put a backslash `\` in front of it.

**Write this:**

```markdown
\*This is not italic\*

\# This is not a heading
```

**Get this:**

\*This is not italic\*

\# This is not a heading

---

## Extended Syntax

The elements above work in almost every Markdown application. The ones below are **extended syntax**. They work on GitHub and in VS Code, but some Markdown applications may not support them.

### Strikethrough

**Write this:**

```markdown
This is ~~wrong~~ right.
```

**Get this:**

This is ~~wrong~~ right.

### Task Lists

**Write this:**

```markdown
- [x] Learn headings
- [x] Learn lists
- [ ] Learn tables
```

**Get this:**

- [x] Learn headings
- [x] Learn lists
- [ ] Learn tables

### Tables

Use `|` to separate columns and `---` to separate the header row from the rest. Colons `:` in the second row control alignment.

**Write this:**

```markdown
| Element | Syntax       | Aligned Right |
| :------ | :----------: | ------------: |
| Bold    | `**text**`   | 1             |
| Italic  | `*text*`     | 2             |
| Link    | `[text](url)`| 3             |
```

**Get this:**

| Element | Syntax       | Aligned Right |
| :------ | :----------: | ------------: |
| Bold    | `**text**`   | 1             |
| Italic  | `*text*`     | 2             |
| Link    | `[text](url)`| 3             |

### Footnotes

**Write this:**

```markdown
Markdown was created in 2004.[^1]

[^1]: It was created by John Gruber.
```

**Get this:**

Markdown was created in 2004.[^1]

[^1]: It was created by John Gruber.

---

## More Information

There are many different "flavors" of Markdown. For example, GitHub has its own flavor called GitHub Flavored Markdown. The basic elements on this page should work everywhere, but extended syntax and links to sections of a page may not work in every Markdown application.

To learn more:

- [Markdown Guide](https://www.markdownguide.org): the basics plus the full extended syntax
- [GitHub's Markdown Guide](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax): everything GitHub supports
