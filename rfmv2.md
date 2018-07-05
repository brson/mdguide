<style>
html {
box-sizing: border-box;
}
*, *:before, *:after {
box-sizing: inherit;
}
body {
margin: 2rem;
max-width: 900px;
margin-left: auto;
margin-right: auto;
font-size: 12pt;
}
h1, h2, h3 {
margin-top: 2rem;
margin-left: -0.5rem;
padding-left: 0.5rem;
padding-bottom: 0.25rem;
}
h1 {
border-bottom: 2px solid black;
border-left: 4px solid black;
}
h2 {
border-bottom: 1px solid black;
border-left: 2px solid black;
}
h3 {
border-bottom: 1px solid gray;
border-left: 2px solid gray;
}
blockquote h1, blockquote h2, blockquote h3 {
border: 0px;
}
</style>

# Reddit-redesign-flavored markdown

A guide to Reddit-flavored markdown, updated for the Reddit
redesign, and current as of 2018/06/14.

- [About this document][about]
- [Quick reference][quick]
- [Where to use markdown in the Reddit redesign][where]
- [Reddit-flavored Markdown syntax][syntax]
  - [Paragraphs and line breaks][para]
  - [Basic text formatting][basic]
  - [Links][links]
  - [Spoilertext][spoil]
  - [Headings][headings]
  - [Lists][lists]
  - [Blockquotes][bq]
  - [Tables][tables]
  - [Code blocks and inline code][code]
  - [Horizontal rules][hr]
- [Tricks and tips][tricks]
  - [Escaping Markdown syntax][esc]
  - [HTML entities][ents]
  - [Tips for robots][bots]
- [Reddit-flavored Markdown recommended practices][rec]
- [Writing Markdown that is compatible with legacy Reddit][legacy]
- [More about Markdown in the Reddit redesign][md]
- [Differences between legacy Reddit, Redesign, and CommonMark][diff]
- [Credits and further reading][cred]
- [Contributing to this document][cont]
- [TODO][todo]

[about]: #about
[quick]: #quick
[where]: #where
[syntax]: #syntax
[para]: #para
[basic]: #basic
[links]: #links
[spoil]: #spoil
[headings]: #headings
[lists]: #lists
[bq]: #bq
[tables]: #tables
[code]: #code
[hr]: #hr
[tricks]: #tricks
[esc]: #esc
[ents]: #ents
[bots]: #bots
[rec]: #rec
[legacy]: #legacy
[md]: #md
[diff]: #diff
[cred]: #cred
[cont]: #cont
[todo]: #todo

<a id="about"/>

## About this document

As the Reddit redesign has rolled out, people have often noted
differences in how content is rendered between "legacy" Reddit and the
redesign. Content on Reddit - comments, self-posts, and otherwise - is
represented as a Reddit-specific variation of the [Markdown] format,
and that format has changed in the redesign.

This is a guide to Reddit-flavored markdown for the redesign era,
explaining generally how to format comments on Reddit, and
specifically identifying areas where redesign Markdown is different
from "legacy" Reddit-flavored markdown.

Within, examples are presented as pairs showing first how the Markdown
is **written** in the editor, then as it is **rendered**, or presented
on the screen. Important *redesign notes* about differences between
redesign Markdown and Reddit legacy markdown are called out in italicized
paragraphs marked with the flour-de-lis (⚜️), and general *tips* with the
crystal ball (&#x1F52E;).

For more technical details see ["More about Markdown in the Reddit
redesign"][md], and ["Differences between legacy Reddit, Redesign, and
CommonMark"][diff].

Some of the content of this document is lifted directly from the
previous work of others. See ["Credits and further reading"][cred] for
details and links.

[Markdown]: https://en.wikipedia.org/wiki/Markdown


<a id="quick"/>

## Quick reference

A condensed cheat-sheet of common Markdown syntax. Read beyond for
details.

### Compatibility syntaxes

### Alternate syntaxes

<a id="where"/>

## Where to use Markdown in the Reddit redesign


<a id="syntax"/>

## Reddit-flavored Markdown syntax


<a id="para"/>

### Paragraphs and line breaks

_Paragraphs_ on Reddit are lines of text separated by blank lines.

**Written**:

> ```
> People think a soul mate is your perfect fit, and that's what
> everyone wants. But a true soul mate is a mirror, the person who shows
> you everything that is holding you back, the person who brings you to
> your own attention so you can change your life.
>
> A true soul mate is probably the most important person you'll ever
> meet, because they tear down your walls and smack you awake. But to
> live with a soul mate forever? Nah. Too painful. Soul mates, they come
> into your life just to reveal another layer of yourself to you, and
> then leave.
>
> A soul mate's purpose is to shake you up, tear apart your ego a
> little bit, show you your obstacles and addictions, break your heart
> open so new light can get in, make you so desperate and out of control
> that you have to transform your life, then introduce you to your
> spiritual master...
> ```

**Rendered**:

> People think a soul mate is your perfect fit, and that's what
> everyone wants. But a true soul mate is a mirror, the person who shows
> you everything that is holding you back, the person who brings you to
> your own attention so you can change your life.
>
> A true soul mate is probably the most important person you'll ever
> meet, because they tear down your walls and smack you awake. But to
> live with a soul mate forever? Nah. Too painful. Soul mates, they come
> into your life just to reveal another layer of yourself to you, and
> then leave.
>
> A soul mate's purpose is to shake you up, tear apart your ego a
> little bit, show you your obstacles and addictions, break your heart
> open so new light can get in, make you so desperate and out of control
> that you have to transform your life, then introduce you to your
> spiritual master...

<a id="hb"/>

Note that _line breaks_ are not displayed - that is, adjacent lines are
concatenated together to create a single paragraph. Line breaks can be
added explitly by ending lines with a backslash ("\\"), or with two
spaces.

**Written**:

> ```
> Out beyond ideas of wrongdoing\
> and rightdoing there is a field.\
> I'll meet you there.
> ```

**Rendered**:

> Out beyond ideas of wrongdoing\
> and rightdoing there is a field.\
> I'll meet you there.

**Written**  (*note the double spaces*):

> ```
> Love is the whole thing.  
> We are only pieces.
> ```

**Rendered**:

> Love is the whole thing.  
> We are only pieces.

⚜️ _**Redesign note**: Creating linebreaks with backslash only works in
redesign. While the backslash is clearer to read and write than two
spaces, if you need compatibility with legacy Reddit, prefer two
spaces._

Paragraphs are separated by any number of blank lines, and those blank
lines are not themselves rendered, thus one can't add an arbitrary
amount of space between paragraphs simply by adding extra blank lines.

**Written**:

> ```
> Be empty of worrying.\
> Think of who created thought!
>
>
>
> Why do you stay in prison\
> When the door is so wide open?
> ```

**Rendered**:

> Be empty of worrying.\
> Think of who created thought!
>
>
>
> Why do you stay in prison\
> When the door is so wide open?

&#x1F52E; _**Tip**: A trick for inserting blanks lines is to create a
paragraph containing nothing but ["non-breaking space"][nbsp] and
explicit linebreaks._

**Written**:

> ```
> Be empty of worrying.\
> Think of who created thought!
>
> &nbsp;\
> &nbsp;
>
> Why do you stay in prison\
> When the door is so wide open?
> ```

**Rendered**:

> Be empty of worrying.\
> Think of who created thought!
>
> &nbsp;\
> &nbsp;
>
> Why do you stay in prison\
> When the door is so wide open?

[nbsp]: https://en.wikipedia.org/wiki/Non-breaking_space


<a id="basic"/>

### Basic text formatting

_Italic_ text is represented by surrounding text with either a single asterisk (`*`) or underscore (`_`).

**Written**:

> ```
> It is *error* only, and not _truth_, that shrinks from inquiry
> ```

**Rendered**:

> It is *error* only, and not _truth_, that shrinks from inquiry

_Bold_ text is represented by surrounding text with either double asterisks (`**`) or double underscores (`__`).

**Written**:

> ```
> It is **error** only, and not __truth__, that shrinks from inquiry
> ```

**Rendered**:

> It is **error** only, and not __truth__, that shrinks from inquiry

_Bold-italic_ text is represented by surrounding text with either triple asterisks (`***`) or triple underscores (`___`).

**Written**:

> ```
> It is ***error*** only, and not ___truth___, that shrinks from inquiry
> ```

**Rendered**:

> It is ***error*** only, and not ___truth___, that shrinks from inquiry

_Strikethrough_ text is represented by surrounding text with double tildes (`~~`).

**Written**:

> ```
> The greatest thing you'll ever learn is just to
> ~~love~~ reddit and be ~~loved~~ reddited in return.
> ```

**Rendered**:

> The greatest thing you'll ever learn is just to
> ~~love~~ reddit and be ~~loved~~ reddited in return.

<a id="super"/>

_Superscript_ is represented by surrounding text in parentheses preceded by a caret (`^`).

**Written**:

> ```
> The greatest thing you'll ever learn is just to
> reddit ^(and be reddited in return).
> ```

**Rendered**:

> The greatest thing you'll ever learn is just to
> reddit ^(and be reddited in return).

A single word can also be superscripted by preceding it with just a caret.

**Written**:

> ```
> The greatest thing you'll ever learn is just to
> ^reddit and be ^reddited in return.
> ```

**Rendered**:

> The greatest thing you'll ever learn is just to
> ^reddit and be ^reddited in return.

⚜️ _**Redesign note**: There are significant differences in the parsing
of superscript between legacy Reddit and redesign. Legacy Reddit in
particular often failed to parse the parethnesized superscript syntax
reasonably. And redesign does not (yet) support multiple levels of
superscript._

&#x1F52E; _**Tip**: For superscript compatibility between legacy and
redesign, stick to the single-word, unparenthesized superscript syntax
and superscript every word, or alternately separate words with
["non-breaking space"][nbsp] HTML entities (`&nbsp;`)._

**Written**:

> ```
> The greatest thing you'll ever learn is just to
> reddit ^and ^be ^reddited ^in ^return.
> ```

**Rendered**:

> The greatest thing you'll ever learn is just to
> reddit ^and ^be ^reddited ^in ^return.

**Written**:

> ```
> The greatest thing you'll ever learn is just to
> reddit ^and&nbsp;be&nbsp;reddited&nbsp;in&nbsp;return.
> ```

**Rendered**:

> The greatest thing you'll ever learn is just to
> reddit ^and&nbsp;be&nbsp;reddited&nbsp;in&nbsp;return.


<a id="spoil"/>

### Spoilertext


<a id="links"/>

### Links

<a id="rlinks"/>

[URLs] beginning with "http://", "https://", or "www." are
automatically [hyperlinked], as are subreddit names ("/r/rust",
"r/rust"), and user names ("/u/spez" and "u/spez"). The latter are
known as "redditlinks" and "userlinks". Collectively these are known
as "autolinks".

|Written|Rendered|
|-|-|
|`http://www.reddit.com`|http://www.reddit.com|
|`https://www.reddit.com`|https://www.reddit.com|
|`www.reddit.com`|www.reddit.com|
|`/r/rust`|/r/rust|
|`r/rust`|r/rust|
|`/u/spez`|/u/spez|
|`u/spez`|u/spez|

[URLs]: https://en.wikipedia.org/wiki/URL
[hyperlinked]: https://en.wikipedia.org/wiki/Hyperlink

&#x1F52E; _**Tip**: Complex URLs can parse in unexpected ways as
autolinks. When you find a URL isn't linking correctly, you can
instead surround the link with angled brackets (`<`, `>`)._

**Written**:

> ```
> <http://example.com/foo/../bar..>
> ```

**Rendered**:

> <http://example.com/foo/../bar..>

Arbitrary text can be explicitly hyperlinked by surrounding it with
square brackets, followed by a URL in parenthesis. The link can
optionally be given a "title", which is typically shown by the browser
when the user hovers their mouse over the link.

The title must be surrounded by single quotes, double quotes, or
parenthesis.

|Written|Rendered|
|-|-|
|`[Rumi](https://en.wikipedia.org/wiki/Rumi)`|[Rumi](https://en.wikipedia.org/wiki/Rumi)|
|`[Zappa](https://en.wikipedia.org/wiki/Frank_Zappa "Frank Zappa - Wikipedia")`|[Zappa](https://en.wikipedia.org/wiki/Frank_Zappa "Frank Zappa")|
|`[Gandhi](https://en.wikipedia.org/wiki/Mahatma_Gandhi 'Mahatma Gandhi - Wikipedia')`|[Gandhi](https://en.wikipedia.org/wiki/Mahatma_Gandhi 'Mahatma Gandhi - Wikipedia')|
|`[Twain](https://en.wikipedia.org/wiki/Mark_Twain (Mark Twain - Wikipedia))`|[Twain](https://en.wikipedia.org/wiki/Mark_Twain (Mark Twain - Wikipedia))|

⚜️ _**Redesign note**: Titles surrounded by paretheses are only
supported in redesign. For compatibility prefer quotes._

Links my also be defined as "references", outside of the paragraph.

**Written**:

> ```
> [Very little] is needed to make a happy life;
> it is all within yourself, in your [way of thinking][wot].
>
> [Very little]: https://www.reddit.com/r/Meditation/
> [wot]: https://psychonautwiki.org/
> ```

**Rendered**:

> [Very little] is needed to make a happy life;
> it is all within yourself, in your [way of thinking][wot].
>
> [Very little]: https://www.reddit.com/r/Meditation/
> [wot]: https://psychonautwiki.org/

By default the reference name is the same as the text in brackets, but
the reference can be named explicitly within a second set of brackets,
as in `[way of thinking][wot]`. Like inline links, reference links can
have titles.

&#x1F52E; _**Tip**: Reference-style links are especially useful for
decluttering text with many links._

**Written**:

> ```
> Somewhere in [la Mancha][lm], in a place whose name I do not care to
> remember, a gentleman lived not long ago, one of those who has a
> [lance] and [ancient shield][as] on a shelf and keeps a [skinny nag][sn]
> and a greyhound for racing.
>
> [lm]: https://en.wikipedia.org/wiki/La_Mancha
> [lance]: https://en.wikipedia.org/wiki/Holy_Lance "Holy Lance - Wikipedia"
> [as]: http://myarmoury.com/feature_shield.html 'The Shield: An Abridged History of its Use and Development'
> [sn]: https://en.wikipedia.org/wiki/Epona (Epona - Wikipedia)
> ```

**Rendered**:

> Somewhere in [la Mancha][lm], in a place whose name I do not care to
> remember, a gentleman lived not long ago, one of those who has a
> [lance] and [ancient shield][as] on a shelf and keeps a [skinny nag][sn]
> and a greyhound for racing.
>
> [lm]: https://en.wikipedia.org/wiki/La_Mancha
> [lance]: https://en.wikipedia.org/wiki/Holy_Lance "Holy Lance - Wikipedia"
> [as]: http://myarmoury.com/feature_shield.html 'The Shield: An Abridged History of its Use and Development'
> [sn]: https://en.wikipedia.org/wiki/Epona (Epona - Wikipedia)

&#x1F52E; _**Tip**: Note that links can only contain parentheses if
they are "balanced", that is, if every "(" is later followed by ")".
To link to a URL with unbalanced parentheses, either escape the
parenthesis with backslash ("\\"), or use the alternate linking syntax,
enclosing the URL in matched angle brackets, "<" and ">"._

**Written**:

> ```
> [Parenthesis](https://en.wikipedia.org/wiki/\()
> ```

**Rendered**:

> [Parenthesis](https://en.wikipedia.org/wiki/\()

**Written**:

> ```
> [Parenthesis](<https://en.wikipedia.org/wiki/(>)
> ```

**Rendered**:

> [Parenthesis](<https://en.wikipedia.org/wiki/(>)


<a id="headings"/>

### Headings

Section _headings_ have six levels and are written with leading hashes (`#`).

**Written**:

> ```
> # Domain
>
> ## Kingdom
>
> ### Phylum
>
> #### Class
>
> ##### Order
>
> ###### Family
> ```

**Rendered**:

> # Domain
>
> ## Kingdom
>
> ### Phylum
>
> #### Class
>
> ##### Order
>
> ###### Family

Level 1 and 2 headers can also be written by underlining the header
text with "=" and "-" respectively.

**Written**:

>```
>Domain
>======
>
>Kingdom
>-------
>```

**Rendered**:

>Domain
>======
>
>Kingdom
>-------


<a id="lists"/>

### Lists

<a id="ol"/>


<a id="tricks"/>

## Tricks and tips


<a id="bots"/>

### Tips for bots

TODO:
- bracketed autolinks
- no spaces between []()
- url-espace some chars
- avoid html entities?
- escape all parens


<a id="rec"/>

## Reddit-flavored Markdown recommended practices

I'm not going to call this "best practices" because that is inviting
contrarianism. These are a few recommendations for writing Markdown
that is compatible with legacy Reddit markdown parsing (so long as the
legacy parser remains in production).


### Easy compatibilty recommendations


### Unfortunate compatibility recommendations


### General recommendations


TODO:
- hardbreaks
- code fences
- superscript
- table pipes
- table header spaces


## More about Markdown in the Reddit redesign

Reddit's redesign markdown parser, snoomark, is a variation of
[GitHub-flavored Markdown (GFM)][gfm], based on [CommonMark], with the
GFM table, and autolink extensions, as well as a modified
strikethrough extension. It also includes Reddit-specific extensions,
and Reddit-specific compatibility quirks that deviate from CommonMark.

snomark is a downstream project of [comrak], which is in turn a
re-implementation of [cmark-gfm], GitHub's CommonMark implementation
with GitHub extensions (GFM), which is in turn downstream of [cmark],
the CommonMark reference implementation.

snomark itself is not (yet) open source, but changes to comrak are
regularly merged into snoomark.

[gfm]: https://github.github.com/gfm/
[CommonMark]: http://commonmark.org/
[comrak]: https://github.com/kivikakk/comrak
[cmark-gfm]: https://github.com/github/cmark
[cmark]: https://github.com/commonmark/cmark

TODO:
- legacy vs commonmark philosophy
- bugs vs features
- migration strategies
- future directions
- adding desirable cm features to r2 (backslash linebreaks especially)
- phasing out of r2 markdown
- RTE vs RTJSON vs Markdown

<a id="diff"/>

## Differences between legacy Reddit, Redesign, and CommonMark

TODO:
- Have links to past /r/redesign discussions.
- Reference for legacy Reddit compatibility / CommonMark compatibility
- Differences from r2 are not comprehensive
- Differences from CM are often to support Reddit quirks

### Reddit-specific extensions

- [Spoilertext][spoil] - Spoilertext (`>!spoiler!<`) is Reddit-specific.
- [Superscript](#super) - There's no superscript standard, and Reddit
  has its own syntax which continues to be supported (`^`, `^(...)`).
- [Redditlinks and userlinks](#rlinks) - Names of subreddits and
  Reddit users, prefixed with `/r/`, `r/`, `/u/, and `u/`, are
  automatically linked.
- [Rich text media](#rtm) - Reddit supports submissions containing
  images, videos, and gifs, and these are encoded into the Markdown.
  This feature is only supported by the RTE (the "fancy pants" editor)
  \- it would be prohibitively difficult to write manually at present.


### New features inherited from CommonMark

- [Ordered lists](#ol) can be written with parentheses in addition to periods
  (`1)` vs. `1.`).
- [Hard line breaks](#hb) can be written by terminating lines with
  `\`, in addition to double-space. This syntax is more readable
  and less surprising than the double-space syntax.
- Nested block elements (like [lists] and [blockquotes][bq] and
  [tables]) can be opened on the same line as list items
- [Code blocks][code] can be written with surrounding fences, instead of
  indentation (`\`\`\`` or `~~~`). This popular syntax is arguably
  more writable and readable than the indentation syntax.


### Differences from legacy Reddit-flavored Markdown

- Unescaped parentheses in links must be balanced.

  - Previous discussions:
    [1](https://new.reddit.com/r/redesign/comments/8cyf5a/download_the_single_art_link_doesnt_work_markdown/)
  - Ticket: CREATE-1662

- Sublists require at least two spaces of indentation for unordered
  lists and three for ordered lists, where legacy reddit only required
  one space.

  - Previous discussions:
    [1](https://new.reddit.com/r/redesign/comments/8eaagg/markdown_rules_for_lists_dont_follow_the_same/)
  - Ticket: CREATE-1702

- The first table header cell cannot be empty if it is not preceded by
  a leading pipe character (`|`), e.g. the following does not work:

  ```
   |B|C
  -|-|-
  d|e|f
  ```

  - Previous discussions:
    [1](https://new.reddit.com/r/redesign/comments/8edfxx/redesign_is_displaying_some_tables_wrong/)
  - Ticket: CREATE-1701

- The first table "marker" cell cannot be a dash followed by a space if
  it is not preceded by a pipe character (`|`) - it will instead be interpreted
  as the beginning of a list, e.g. the following does not work:

  ```
  A | B
  - | -
  c | d
  ```

  - Previous discussions:
    [1](https://new.reddit.com/r/redesign/comments/8eter9/table_not_parsed_on_redesign_if_second_row_starts/)
  - Ticket: CREATE-1708

- Spoilertext does not to be ["flanking"], i.e. the spoilertext delimiters
  (`>!` and `!<`) will be parsed as such regardless of their adjacency to
  whitespace and punctuation.

  - Previous discussions:
    [1](https://www.reddit.com/r/redesign/comments/8s0qyy/old_inline_spoiler_bug_still_around/)
  - Ticket: CREATE-1534

["flanking"]: https://github.github.com/gfm/#left-flanking-delimiter-run

- Link syntax does not allow space between the square brackets (`[]`) and
  the parenthesis (`()`).

  - Previous discussions:
    [1](https://www.reddit.com/r/redesign/comments/86qve1/imgur_album_links_dont_work_embedded_or_stand/)
    [2](https://new.reddit.com/r/redesign/comments/8bhpca/hyperlinks_with_space_between_both_elements_are/)
  - Ticket: CREATE-1438


### Differences from CommonMark / GFM


<a id="cred"/>

## Credits and further reading

The basic organization of this page and its requirements were inspired
by - and content sometimes direcly lifted from - /u/AnteChrono's
[Reddit Markdown Primer][prime], /u/Raerth's [Reddit Comment
Formatting][fmt], and the existing ["commenting" wiki page][cmt].

Quotes used as examples:

- "People think a soul mate is your perfect fit..." - [Elizabeth Gilbert], from Eat, Pray, Love
- "Out beyond ideas of wrongdoing...", "Love is the whole thing...", "Be empty of worrying..." - [Rumi]
- "Very little is needed to make a happy life..." - [Marcus Aurelius]
- "It is error only..." - [Thomas Paine]
- "The greatest thing you'll ever learn..." - [eden ahbez]

[Elizabeth Gilbert]: https://en.wikipedia.org/wiki/Elizabeth_Gilbert
[Rumi]: https://en.wikipedia.org/wiki/Rumi
[Marcus Aurelius]: https://en.wikipedia.org/wiki/Marcus_Aurelius
[Thomas Paine]: https://en.wikipedia.org/wiki/Thomas_Paine
[eden ahbez]: https://en.wikipedia.org/wiki/Eden_ahbez

[prime]: https://www.reddit.com/r/reddit.com/comments/6ewgt/reddit_markdown_primer_or_how_do_you_do_all_that/c03nik6/
[fmt]: https://www.reddit.com/r/raerth/comments/cw70q/reddit_comment_formatting/
[cmt]: https://www.reddit.com/wiki/commenting


<a id="cont"/>

## Contributing to this document


<a id="todo"/>

## TODO

- What to call RFM and RFMv2
  - CommonMark-flavored Reddit-flavored Markdown (CMRFM)
  - Reddit-flavored CommonMark (RFCM)
  - CommonMark Reddit-flavored Markdown (CM-RFM)
- Interior emph with *