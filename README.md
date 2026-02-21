# al-folio


## Table Of Contents

<!--ts-->

- [al-folio](#al-folio)
  - [Table Of Contents](#table-of-contents)
  - [Getting started](#getting-started)
  - [Installing and Deploying](#installing-and-deploying)
  - [Customizing](#customizing)
  - [GitHub Copilot Agents](#github-copilot-agents)
    - [Customization Agent](#customization-agent)
    - [Documentation Agent](#documentation-agent)
  - [Documentation](#documentation)
  - [Features](#features)
    - [CV](#cv)
    - [Publications](#publications)
    - [Collections](#collections)
    - [Layouts](#layouts)
      - [The iconic style of Distill](#the-iconic-style-of-distill)
      - [Full support for math &amp; code](#full-support-for-math--code)
      - [Photos, Audio, Video and more](#photos-audio-video-and-more)
    - [Other features](#other-features)
      - [GitHub's repositories and user stats](#githubs-repositories-and-user-stats)
      - [Theming](#theming)
      - [Social media previews](#social-media-previews)
      - [Atom (RSS-like) Feed](#atom-rss-like-feed)
      - [Related posts](#related-posts)
      - [Code quality checks](#code-quality-checks)
      - [GDPR Cookie Consent Dialog](#gdpr-cookie-consent-dialog)
  - [FAQ](#faq)
  - [License](#license)

<!--te-->

## Getting started

**⚠️ Important: Use "Use this template" (not fork)**

For quick setup, see [QUICKSTART.md](QUICKSTART.md).

## Installing and Deploying

For installation and deployment details please refer to [INSTALL.md](INSTALL.md).

## Customizing

For customization details please refer to [CUSTOMIZE.md](CUSTOMIZE.md).

## GitHub Copilot Agents

This repository includes two specialized GitHub Copilot agents to enhance your development experience:

### Customization Agent

The **Customization Agent** helps you personalize your al-folio website by:

- Guiding you through configuration changes step-by-step
- Modifying files directly in your repository
- Explaining technical concepts in plain language (great for users without coding experience)
- Assisting with common tasks like updating your CV, adding publications, creating blog posts, and customizing themes

See [CUSTOMIZE.md § GitHub Copilot Customization Agent](CUSTOMIZE.md#github-copilot-customization-agent) for detailed usage instructions.

### Documentation Agent

The **Documentation Agent** maintains clear and up-to-date project documentation by:

- Updating documentation files when features change
- Writing in a style accessible to academics and researchers
- Keeping documentation synchronized with the codebase
- Following documentation best practices

See [CONTRIBUTING.md § GitHub Copilot Agents](CONTRIBUTING.md#github-copilot-agents) for more information.

> **Requirements:** Both agents require a [GitHub Copilot](https://github.com/features/copilot) subscription. For more information about GitHub Copilot and how to use agents, see the [GitHub Copilot documentation](https://docs.github.com/en/copilot).

## Documentation

Comprehensive guides for all aspects of your al-folio website:

- **[Quick Start](QUICKSTART.md)** – Get running in 5 minutes
- **[Installation & Deployment](INSTALL.md)** – Set up your site on GitHub Pages or other platforms
- **[Customization Guide](CUSTOMIZE.md)** – Personalize your website (CVs, publications, themes, etc.)
- **[Troubleshooting](TROUBLESHOOTING.md)** – Fix common issues (deployment, build, styling, content)
- **[FAQ](FAQ.md)** – Frequently asked questions and solutions
- **[Analytics](ANALYTICS.md)** – Add website analytics and visitor tracking
- **[SEO Guide](SEO.md)** – Optimize for search engines and improve discoverability

## Features

### CV

Your CV can be generated in one of two modern formats: **RenderCV** (recommended, with automatic PDF generation) or **JSONResume** (standardized JSON format). You can use both simultaneously and switch between them, or maintain just the one you prefer.

[![CV Preview](readme_preview/cv.png)](https://alshedivat.github.io/al-folio/cv/)

For setup and customization details, see [Modifying the CV information](CUSTOMIZE.md#modifying-the-cv-information) in [CUSTOMIZE.md](CUSTOMIZE.md).

---

### Publications

Your publications page is generated automatically from your BibTeX bibliography. You can customize publication display, add extra information like PDFs, and control sorting behavior.

[![Publications Preview](readme_preview/publications.png)](https://alshedivat.github.io/al-folio/publications/)

For setup, BibTeX field documentation, and customization options, see [Adding a new publication](CUSTOMIZE.md#adding-a-new-publication) and [Managing publication display](CUSTOMIZE.md#managing-publication-display) in [CUSTOMIZE.md](CUSTOMIZE.md).

---

### Collections

This Jekyll theme implements `collections` to organize content into categories. The theme comes with default collections for `news`, `projects`, `books`, and `teachings`. You can easily create your own collections for apps, stories, courses, or any other creative work.

[![Projects Preview](readme_preview/projects.png)](https://alshedivat.github.io/al-folio/projects/)

For detailed instructions on creating and customizing collections, see [Adding Collections](CUSTOMIZE.md#adding-collections) in [CUSTOMIZE.md](CUSTOMIZE.md).

---

### Layouts

**al-folio** comes with stylish layouts for pages and blog posts.

#### The iconic style of Distill

The theme allows you to create blog posts in the [distill.pub](https://distill.pub/) style:

[![Distill Preview](readme_preview/distill.png)](https://alshedivat.github.io/al-folio/blog/2021/distill/)

For more details on how to create distill-styled posts using `<d-*>` tags, please refer to [the example](https://alshedivat.github.io/al-folio/blog/2021/distill/).

#### Full support for math & code

**al-folio** supports fast math typesetting through [MathJax](https://www.mathjax.org/) and code syntax highlighting using [GitHub style](https://github.com/jwarby/jekyll-pygments-themes). Also supports [chartjs charts](https://www.chartjs.org/), [mermaid diagrams](https://mermaid-js.github.io/mermaid/#/), and [TikZ figures](https://tikzjax.com/).

<p align="center">
<a href="https://alshedivat.github.io/al-folio/blog/2015/math/" target="_blank"><img src="readme_preview/math.png" width=400></a>
<a href="https://alshedivat.github.io/al-folio/blog/2015/code/" target="_blank"><img src="readme_preview/code.png" width=400></a>
</p>

#### Photos, Audio, Video and more

Photo formatting is made simple using [Bootstrap's grid system](https://getbootstrap.com/docs/4.4/layout/grid/). Easily create beautiful grids within your blog posts and project pages, also with support for [video](https://alshedivat.github.io/al-folio/blog/2023/videos/) and [audio](https://alshedivat.github.io/al-folio/blog/2023/audios/) embeds:

<p align="center">
  <a href="https://alshedivat.github.io/al-folio/projects/1_project/">
    <img src="readme_preview/photos-screenshot.png" width="75%">
  </a>
</p>

---

### Other features

#### GitHub's repositories and user stats

**al-folio** displays GitHub repositories and user stats on the `/repositories/` page using [github-readme-stats](https://github.com/anuraghazra/github-readme-stats) and [github-profile-trophy](https://github.com/ryo-ma/github-profile-trophy).

[![Repositories Preview](readme_preview/repositories.png)](https://alshedivat.github.io/al-folio/repositories/)

To configure which repositories and GitHub profiles to display, see [Modifying the user and repository information](CUSTOMIZE.md#modifying-the-user-and-repository-information) in [CUSTOMIZE.md](CUSTOMIZE.md).

---

#### Theming

**al-folio** offers a variety of beautiful theme colors to choose from. The default is purple, but you can customize colors, fonts, spacing, and more to match your style.

For detailed customization instructions, see [Changing theme color](CUSTOMIZE.md#changing-theme-color) and [Customizing fonts, spacing, and more](CUSTOMIZE.md#customizing-fonts-spacing-and-more) in [CUSTOMIZE.md](CUSTOMIZE.md).

---

#### Social media previews

**al-folio** supports Open Graph preview images on social media. When enabled, your site's pages display rich preview objects with images, titles, and descriptions when shared.

For setup and customization, see [Social media previews](CUSTOMIZE.md#social-media-previews) in [CUSTOMIZE.md](CUSTOMIZE.md).

---

#### Atom (RSS-like) Feed

It generates an Atom (RSS-like) feed of your posts, useful for Atom and RSS readers. The feed is reachable simply by typing after your homepage `/feed.xml`. E.g. assuming your website mountpoint is the main folder, you can type `yourusername.github.io/feed.xml`

---

#### Related posts

By default, blog posts display related posts at the bottom. These are selected by finding the most recent posts that share tags with the current post. You can customize this behavior on a per-post or site-wide basis.

For configuration details, see [Related posts](CUSTOMIZE.md#related-posts) in [CUSTOMIZE.md](CUSTOMIZE.md).

---

#### Code quality checks

Currently, we run some checks to ensure that the code quality and generated site are good. The checks are done using GitHub Actions and the following tools:

- [Prettier](https://prettier.io/) - check if the formatting of the code follows the style guide
- [lychee](https://lychee.cli.rs/) - check for broken links
- [Axe](https://github.com/dequelabs/axe-core) (need to run manually) - do some accessibility testing

We decided to keep `Axe` runs manual because fixing the issues are not straightforward and might be hard for people without web development knowledge.

---

#### GDPR Cookie Consent Dialog

**al-folio** includes a built-in, GDPR-compliant cookie consent dialog to ensure your website respects visitor privacy. The dialog is powered by [Vanilla Cookie Consent](https://cookieconsent.orestbida.com/) and integrates seamlessly with all supported analytics providers.

When enabled, analytics scripts are blocked until the user explicitly consents, and user preferences are saved across visits. This is essential for websites serving visitors in the European Union and other regions with strict privacy regulations.

For complete setup and customization details, see [GDPR Cookie Consent Dialog](#gdpr-cookie-consent-dialog) in [CUSTOMIZE.md](CUSTOMIZE.md).

## FAQ

For frequently asked questions, please refer to [FAQ.md](FAQ.md).

## License

The theme is available as open source under the terms of the [MIT License](https://github.com/alshedivat/al-folio/blob/main/LICENSE).

Originally, **al-folio** was based on the [\*folio theme](https://github.com/bogoli/-folio) (published by [Lia Bogoev](https://liabogoev.com) and under the MIT license). Since then, it got a full re-write of the styles and many additional cool features.
