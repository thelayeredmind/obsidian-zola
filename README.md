# Obsidian-Zola

This repo contains an easy-to-use (read: simplistic) solution for converting an Obsidian Personal Knowledge Management System (read: bunch of random Markdowns) into a Zola site.

Disclaimer: This repo is forked from the [Adidoks](https://github.com/aaranxu/adidoks) theme. However, several changes are made to alter / improve the use experience.

## Usage

**Step 1: Change Obsidian Settings**
- Set `Settings => Files & Links => New link format`to Relative path to file
- Set `Settings => Files & Links => Use [[Wikilinks]]` to off

** Step 2: Modify Existing Obsidian Links
- Install and activate the `Obsidian Link Converter` plugin
- Set `Obsidian Link Converter => Converted Link Format` to `Relative Path`
- Run command `Obsidian Link Converter: Vault: Links to Wiki` then `Obsidian Link Converter: Vault: Links to Markdown`

*The reason to run the command twice is to convert existing Markdown links to relative links also*

**Step 3: Setup Netlify**
- Turn your Obsidian vault folder into a Git repository
- Create a Netlify site pointing to that Git repository

**Step 4: Edit `netlify.toml`**
- Create `netlify.toml` in your Obsidian vault folder
- Copy the content from `netlify.example.toml` in this repo and replace the placeholders

**Step 5: You're Done!**
Push your changes and enjoy your new site!

## Examples
[Example site](https://peteryuen.netlify.app/)

[Example repo](https://github.com/ppeetteerrs/obsidian-pkm)

## Obsidian Features

**Disclaimer**

> This tool is made for people who use Obsidian as a simple and efficient note-taking app (or PKM). If you configured your Obsidian with plenty of fancy shortcodes, plugins and Obsidian-specific syntax, this tool would not (and does not intend) to support those features.

**Supported**
- Typical Markdown syntax
- Strikethroughs
- Tables
- Single-line footnotes (i.e. `[^1]` in the paragraph and `[^1]: xxx` later)
- Checkboxes
- Link escaping pattern: `[Slides Demo](<Slides Demo>)`

**Unsupported**

- Non-image embeds (e.g. notes, videos, audio, PDF)
- Image resizing
- Highlighting text
- Comments
- Inline / Multi-line footnotes
- Mermaid Diagrams

## Zola Features (vs the original AdiDoks)

First of all, this repo is fully customized for Obsidian PKMs. Of course you can still use it like a regular Zola theme, but it might lack some flexibility in terms of customization.

### Enhancements

**Search Function**

Partial strings are supported now. Since PKM often invole plenty of jargons and the default elasticlunr (of course) cannot do proper stemming on those words, partial string search is an absolute must when it comes to PKM searching.

**Fonts**

Changed default font to Inter for a neater interface.

Changed monospace font to Fira Code because who doesn't love font ligatures?

**KaTEX**

Updated KaTEX to latest version and loads KaTEX by default. Since who on earth builds a PKM without any LaTEX :)

**Table of Content**

Again, who wants to write a PKM page without proper TOC navigation :))

### Small Chanages

**Change Default Content**

Default footers, licenses and menu items are gone. Bye and see you never!

**Example Site Materials**

Deleted example site content and stuff to prevent a bloated repo :)