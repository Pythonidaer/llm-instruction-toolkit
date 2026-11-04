# Source file basics — TS/JS review instructions

Adapted from Google's [TS/JS Style Guide](https://google.github.io/styleguide/tsguide.html#source-file-basics), source blob `89c4630754647df4b2dc3ebabef33276f6eeece1`. Google and contributors; [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/). This adaptation adds application checks, removes presentation wrappers and expands internal links. No Google endorsement is implied.

Read [scope and precedence](README.md) and the [React/Vite applicability profile](react-vite-profile.md) first. The profile's explicit exceptions override the corresponding source rules. Other applicable source rules below retain their original strength. Source examples are illustrative, not additional requirements.

## Application checks

- **TS2.1:** Save UTF-8 source; avoid invisible whitespace outside deliberate escaped strings.
- **TS2.2:** Use readable Unicode for printable text; explain necessary non-printing characters.
- **TS2.3:** Do not rewrite user-facing copy as a side effect of code formatting.

## Detailed baseline, including source subsections

The retained source text below supplies the detailed rules, rationale and exceptions. Consult it for the specific pattern under review; do not infer missing constraints from the short checks above.

## Source file basics

<a id="file-encoding"></a>

<a id="file-encoding-utf-8"></a>

### File encoding: UTF-8

Source files are encoded in **UTF-8**.

<a id="special-characters"></a>

<a id="whitespace-characters"></a>

#### Whitespace characters

Aside from the line terminator sequence, the ASCII horizontal space character
(0x20) is the only whitespace character that appears anywhere in a source file.
This implies that all other whitespace characters in string literals are
escaped.

<a id="special-escape-sequences"></a>

#### Special escape sequences

For any character that has a special escape sequence (`\'`, `\"`, `\\ `, `\b`,
`\f`, `\n`, `\r`, `\t`, `\v`), that sequence is used rather than the
corresponding numeric escape (e.g `\x0a`, `\u000a`, or `\u{a}`). Legacy octal
escapes are never used.

<a id="non-ascii-characters"></a>

#### Non-ASCII characters

For the remaining non-ASCII characters, use the actual Unicode character (e.g.
`∞`). For non-printable characters, the equivalent hex or Unicode escapes (e.g.
`\u221e`) can be used along with an explanatory comment.

```ts
// Perfectly clear, even without a comment.
const units = 'μs';

// Use escapes for non-printable characters.
const output = '\ufeff' + content;  // byte order mark
```

```ts
// Hard to read and prone to mistakes, even with the comment.
const units = '\u03bcs'; // Greek letter mu, 's'

// The reader has no idea what this is.
const output = '\ufeff' + content;
```

<a id="modules"></a>
<a id="source-organization"></a>

<a id="source-file-structure"></a>
