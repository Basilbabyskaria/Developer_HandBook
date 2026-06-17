# How to Write a ReadMe File

## Markdown

Markdown is a lightweight markup language which used by Github and Others. It allows users to format text using a plain-text editor, making it easy to create formatted documents without the need for complex HTML tags. Markdown is essentially rendered as HTML

## Flavour's

Mardown actually have different flavours used by different creators. Features of some may not work on other's

## Line Break

If you want to keep text's in
seperate line's do a double space after the first line,  
 other wise even if you write the text's in seperate lines it will be rendered as a big paragraph ignoreing it as space. Double space after the end of first line render's a `<br>` tag in HTML.

Or just seperate it by an empty Line

## Comments

`[comment]: <> (comment)`  
`[//]: <> (comment)`

## ` BackTik (Escape Sequence)

To render things That usually are used to render other things.  
`#` Headings  
`<BR>` Tags

```
Three ` can Render Code
```

## Headings

H1 Heading :- `#`  
H2 Heading :- `##`  
H3 Heading :- `###`

And so on... to 6

## Bold

`**` :- Makes Text **Bolder**  
`_ _` :- Makes Text **Bolder**

## Italic

`*` :- Makes Text _Italic_  
`_` :- Makes Text _Italic_

## Bold And Italic

`***` :- Makes Text ***Boldtalic***  

`_ _ _` :- Makes Text **_Boldtalic_**

## Crossed off

`~~` :- Makes Text ~~Crossed Off~~

## Highlight

`==` :- Highlights, but does not work on GitHub  
GitHub Supports HTML scripting so we can use this for the same result.  
<mark>Highlight</mark>

## Super Sub Scripting

Can Surround a text with `^` for super and `~` for sub but again does not work on GitHub and need to use `<SUB>` and `<SUP>` instead  
H<SUB>2</SUB>0 ` `A<SUP>2</SUP>

## Emoji 😒

Copy Paste Emoji for GitHub  
Use`: Emojie Name :` For Others  
Use `🪟+.` for Emoji

## Links

Use `[Name](Link)`  
External :- [External Link Name](www.google.com)  
Internal :- [Internal Link To Headings](/README/How_To_Write_a_Readme.md)

## Images

Use `~[altTrext](Link)`  
~[Git](https://images.app.goo.gl/NcK9ArqViCwCbBbq8)

## Horizontal Rule

`---` ,`***`,`___`

---

---

---

## List

Number Followed by `.` allways returns a Ordered list

1. item 1
2. item 2

---

For UnOrdered List use `*` ,`-` or `+`

- item 1
  - item 2
    - item 3
      - item 4

For Nesting Use Tab key

## > (qoute)

> 1 `>`
>
> > 2 `>>`
> >
> > > 3 `>>>`

`>` Gives This

## Table (Git)

Use `|` for start and end of each column  
Use `----` for seperating heading row with others
And use `:----:` Aligning Items to Center in Each Column

```

|H1|H2|
|----|:----:|
|i1|i2|
```

| H1  | H2  |
| --- | :-: |
| i1  | i2  |

## Check Box (Git)

For UNChecked Check Box `-[] text`
For Checked Check Box `-[X] text`

-[] text  
-[X] text
