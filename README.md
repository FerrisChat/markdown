# FerrisChat's Markdown Standard
This README will contain the entire markdown standard to be used by parsers that parse plain, boring message content into ones with ***style***.

## Markdown Parsers
All *official* parsers are open-source. Their source code can be found in this repository.

## The Standard
This will hereby begin the official markdown standard for FerrisChat chat messages.

### Table of Contents
[Introduction](#Introduction)

### Introduction
FerrisChat's Markdown Standard inherits a majority of it's syntax from [CommonMark](https://commonmark.org/).

#### Example Format
All examples of markdown syntax will be displayed in the following format:

###### Example

|          Raw         |       Rich       |           HTML          |
| -------------------- | ---------------- | ----------------------- |
| \*\*example text\*\* | **example text** | ``<b>example text</b>`` |

### CommonMark inherited syntax
This section will go over markdown syntax that were completely inherited from CommonMark.

#### Bold/Strong text
Two asterisks (\*) placed both before and after text will make said text bold or strong.

###### Example

|          Raw         |       Rich       |           HTML          |
| -------------------- | ---------------- | ----------------------- |
| \*\*example text\*\* | **example text** | ``<b>example text</b>`` |

##### Note
Two underscores (\_) placed both before and after text will *not* make said text bold or strong,
unlike in CommonMark. The behavior of this syntax can be found at [Underlines](#Underlines).

#### Italics
One asterisk placed both before and after text will make said text italicized, or slanted.  
A single underscore (\_) placed both before and after said text will also make the text italicized.

###### Examples

|        Raw       |      Rich      |           HTML          |
| ---------------- | -------------- | ----------------------- |
| \*example text\* | *example text* | ``<i>example text</i>`` |
| \_example text\_ | _example text_ | ``<i>example text</i>`` |

#### Strikethrough
Two tildes (\~) placed before and after text will add a line over the center of the text, more commonly
referred to as a "strikethrough".

###### Examples

|          Raw         |       Rich       |           HTML          |
| -------------------- | ---------------- | ----------------------- |
| \~\~example text\~\~ | ~~example text~~ | ``<s>example text</s>`` |

#### Embedded Inline Code
One or two backticks (\`) placed both before and after text will render the text in a monospaced font.
Said text is usually pieces of code, hence the name "inline code".

###### Examples

|          Raw         |       Rich       |              HTML             |
| -------------------- | ---------------- | ----------------------------- |
|   \`example text\`   |  `example text`  | ``<code>example text</code>`` |
| \`\`example text\`\` | ``example text`` | ``<code>example text</code>`` |

#### Embedded Block Code (Code-blocks)
Three backticks placed both before and after text will render the text as a block with a distinct background and a monospaced font.
Said text is usually blocks of code, hence the name "code-block".

##### Adding Syntax Highlighting
Adding a valid syntax language code, followed by a newline right after the first 3 backticks with no space in-between will add syntax-highlighting to the code-block.

For example, here we are adding syntax-highlighting to a Python code-block:
\`\`\`py
...\`\`\`

Trailing newlines in the code-block will not be rendered.

|          Raw         |       Rich       |              HTML             |
| -------------------- | ---------------- | ----------------------------- |
| \`\`\`<br>example text<br>\`\`\` |  ```example text```  | ``<pre><code>example text</code></pre>`` |
| \`\`\`py<br>print('Hello, world!')<br>\`\`\` | ```py
print('Hello, world!')
``` | ``<pre data-language="py"><code>...</code></pre>`` |
