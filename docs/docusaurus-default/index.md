# Tutorial Intro

Let's discover **Docusaurus in less than 5 minutes**.

## Getting Started

Get started by **creating a new site**.

Or **try Docusaurus immediately** with **[docusaurus.new](https://docusaurus.new)**.

### What you'll need

- [Node.js](https://nodejs.org/en/download/) version 16.14 or above:
  - When installing Node.js, you are recommended to check all checkboxes related to dependencies.

## Generate a new site

Generate a new Docusaurus site using the **classic template**.

The classic template will automatically be added to your project after you run the command:

```bash
npm init docusaurus@latest my-website classic
```

You can type this command into Command Prompt, Powershell, Terminal, or any other integrated terminal of your code editor.

The command also installs all necessary dependencies you need to run Docusaurus.

## Start your site

Run the development server:

```bash
cd my-website
npm run start
```

The `cd` command changes the directory you're working with. In order to work with your newly created Docusaurus site, you'll need to navigate the terminal there.

The `npm run start` command builds your website locally and serves it through a development server, ready for you to view at http://localhost:3000/.

Open `docs/intro.md` (this page) and edit some lines: the site **reloads automatically** and displays your changes.


:::info

This page has been slightly adapted to retain the standard structure, even though this file is no longer the root file. 
Adaption are made as found in https://github.com/facebook/docusaurus/blob/main/website/docs/guides/docs/sidebar/index.md

The following was done:

- adapted folder structure:
  ```bash
  website # root directory of your site
  ├── docs
  │   └── my new welcome doc.md
  │   └── docusaurus-default
  │       └── index.md (old `intro.md`)
  │       └── tutorial-basics
  │           └── ...(default)
  │       └── tutorial-extras
  │           └── ...(default)  
  ├── ...
  ```
- renamed the the default `intro.md` to `index.md`.
- added `mdx`as found in [in the source of Sidebar-Doc](https://github.com/facebook/docusaurus/blob/main/website/docs/guides/docs/sidebar/index.md).
  ````bash
  §```mdx-code-block
  import DocCardList from '@theme/DocCardList';
  import {useCurrentSidebarCategory} from '@docusaurus/theme-common';
  
  <DocCardList items={useCurrentSidebarCategory().items}/>
  ```
  ````



:::

```mdx-code-block
import DocCardList from '@theme/DocCardList';
import {useCurrentSidebarCategory} from '@docusaurus/theme-common';

<DocCardList items={useCurrentSidebarCategory().items}/>
```

