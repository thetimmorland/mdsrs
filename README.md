# MDSRS - Markdown Spaced Repetition System

A spaced repetition system similar to [Anki](https://apps.ankiweb.net/) where cards are created by writing plain markdown notes.

<!-- ## Idea

There are two reasons we take notes

1. To create a reference we can consult later
2. To help us remember things without having to look them up

Markdown has proven itself as a great easily-searchable format for taking note takin -->

## Syntax

MDSRS Parses all `**/*.md` files in its starting directory and uses those files to create flash cards.

Basic Cards (Front and Back) can be defined in lists anywhere in your markdown file.

```md
- front: back
```

Basic Cards can also be defined using the [definition list](https://michelf.ca/projects/php-markdown/extra/#def-list) syntax from PHP Markdown Extra.

[Cloze](https://en.wikipedia.org/wiki/Cloze_test) cards are also supported by using the form `{{ommited}}` in any list item in your markdown file. The body of the cloze will be the rest of the list item.

```md
# Rust

## Stack vs Heap

- In Rust values are {{stack}} allocated by default.
```

All prompts are prepended with their associated headings to add context. So the above cloze card's prompt will appear as: `Rust::Stack vs Heap::In Rust values are [?] allocated by default.`.
