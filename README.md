# markdown-content

This repository contains the user facing documentation that populates
app.stateless.solutions/documentation.

## Navigation and Sections

The order of navigation categories is contained in the `SECTIONS.md` file.

This file contains yaml front matter (enclosed in `---` at the top of the
page)that only exists to define the order of the higher level sections.

The only key in the frontmatter should be `"section"`, and the name for each
category should be kept in quotes how it will display in the navigation bar.

The order of the bullet list defines the order of the sections in the
navigation bar.

I.e.

```yaml
sections:
     - "Get Started"
     - "Developer Guides"
     - "Provider Guides"
     - "Deverloper Reference"
```

## Content

Every other markdown file at the root of the repo is assumed to be a content
page. Each of these pages needs the following font matter defined:

```yaml
section: "Section Name as Defined in Sections"
sortOrder: 1
label: "Navigation Section Display Label"
pageName: "Name of the page for the url"
```

Important that the `section` name match a defined name as defined in the
`SECTIONS.md` file.

With a section defined, the `sortOrder` is relative only to other pages within
that section. So if there are only 2 pages in a section, the `sortOrder` of
those pages should be no greater than 2.

The `label` defines what the Navigation bar will display.

And the `pageName` should only be the final URL slug for the name of the page.
This should not include any paths, but it should be only defined by URL safe
parameters.
