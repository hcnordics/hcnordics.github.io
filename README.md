# Human Capital in the Nordic Countries
This GitHub repository hosts files for the project website, and is intended for use only by project team members. The project website can be found at: https://hcnordics.github.io/

# Editing the website
The website is constructed with GitHub pages using files written in Markdown (.md). Markdown is simple, providing a minimal amount of formatting using a text-based editor.

This brief guide to editing the website discusses:
1. which [folders and files](#folders-and-files) can be edited
1. how to [format pages using Markdown](#formatting-in-markdown)
1. where details of [team members](#listing-team-members) are saved

## Folders and files
The website's content is located in the main directory (where you are now), and the folders:
- `_projects` (containing pages for each project group)  
- `_research` (containing pages for each individual piece of research)
- `_sources` (containing pages that describe our source materials, and track progress relating to them).

The other folders contain the nuts and bolts of the site and its design. Please only edit files in the folders listed above! 😊

### Editing and saving
To edit the content of a website page, click on the relevant Markdown (.md) file here in GitHub, then find the pencil icon ("Edit this file"). This will open up the editor, where you can make changes to the page's text. When you are finished editing, scroll down and click on the green _Commit changes_ button: this will save the updated page content.

Any changes you make to the site will not appear immediately. Rather, edits require the site to be recompiled, which may take a few minutes. (Note that you may need to refresh the page.) You will be notified in the event of any compilation errors which prevent the changes from being adopted. 

### The instruction block
Each Markdown (.md) file includes basic instructions to generate the page. At a minimum, this includes the page _title_ and _layout_ (usually "default"). Other prompts that can be included in the instruction block are:
- _subtitle_: An extension of the page title. Particularly relevant for research items.
- _shorttitle_: An abbreviated title that can be used where space is constrained. This is currently only used for project groups, where short titles are used in some site links.
- _status_: An optional one-word descriptor for research items. Useful for noting that a paper is ["Completed"](https://hcnordics.github.io/research/rivista).
- _cover_: Allows a cover image for the page title. Images must be saved in the `assets/images/header` directory. Contact Nick if there's a specific image you want to include!
- _members_: Lists the project team members that are assigned to the relevant item (eg. a research item). Individuals are identified by surname (or a username), separated by commas and included in square brackets (see below).
- _projects_: Lists the project groups that a research item is attached to. Projects are identified by the filename "slug" (everything before the `.md` extension) for the relevant project. As with _members_ above, you can list multiple projects within square brackets.

Only include those items that you need for the page. In many cases, _title: "INSERT TITLE HERE"_ and _layout: default_ will be sufficient.

The instruction block starts and ends with three dashes:
```
---
title: "This is the title of a paper"
subtitle: "And it also has a subtitle"
members: [Jensen, Hansen, Christiansen]
layout: default
---

Here is the first line of text on the page.
```

The page content immediately follows the instruction block as plain text. The page title (along with any subtitle) is coded into the template -- as such, you do not need to manually enter the title in the page content.

## Formatting in Markdown
The benefit of Markdown is its simplicity: just insert your text, and the template takes care of the rest! There is a limited range of formatting available to structure the text and highlight information.
```
## Heading
### Sub-heading

_Italics_
**Bold**

Here is an unordered list:
- with this dot point marked by a dash
- followed by another dot point
  - with an indented sub-point
  - which you get by hitting the tab key, then typing a dash
- and a concluding dot point.

Ordered lists are also possible:
1. This is the first point.
2. Note that you can just mark all points as "1."
3. This will still produce a correctly numbered list.
```

Website links and images can also be included:
```
[text for a link](https://www.yourwebsitehere.com)

![description of an image](image.jpg)
````

We also use tables on the HCNC website, particularly to provide an overview of our source material. Tables are the most complicated piece of Markdown coding: essentially, you have to draw the table using text notation. Each row is a new line of text, each column is separated by a vertical pipe (|), while the table header is separated by dashes (---). An example of a table is:
```
| Navn | By | Dato | Arbejde | 
| --- | --- | --- | --- |
| Jens | Hillerød | 23-06 | Kok |
| Hans | Aalborg | 10-07 | Gartner |
```
When the page is generated, you then get:

| Navn | By | Dato | Arbejde | 
| --- | --- | --- | --- |
| Jens | Hillerød | 23-06 | Kok |
| Hans | Aalborg | 10-07 | Gartner |

(Note that you cannot colour table cells.)

A more complete overview of Markdown coding can be found at the [Markdown Guide](https://www.markdownguide.org/cheat-sheet/).

## Listing team members
Project team members are coded into the configuration file for the website (`_config.yml` in the main directory). Each individual is listed using the following format in the section headed _team_:
```
  - surname: ""
    firstname: ""
    position: ""
    institution: ""
    website: ""
    twitter: ""
    github: ""
```
(Note the dash before surname: this marks the start of an individual's entry.)

The above values are used to populate the team member profile boxes that appear on the site -- for example, on the [About HCNC](https://hcnordics.github.io/about/) page.

As noted above, _surname_ is the value used to identify team members where individuals are assigned to pages using the _members_ option in the instruction block. Alternatively -- and especially for cases where a surname is shared by multiple individuals -- a _username_ field can also be included: just add an extra line below _firstname_ with `username: "NAME HERE"`. To avoid confusion, usernames should be entirely lower case (eg. "ford_n").

In addition, _role_ can also be included to define specific tasks. At this stage, _role_ is only used to denote those with responsibilities for managing this GitHub. 

You are welcome to edit your own profile information, but otherwise avoid editing the configuration file, as this may "break" the website!

# About the site
This GitHub Pages site was set up by [Nick Ford](https://github.com/nickforddk), using a heavily edited version of the Jekyll template, _Dinky_. The typeface is the open source variable font [Archivo](https://fonts.google.com/specimen/Archivo).
