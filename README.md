# Code for Milwaukee Website

## Installation

1. [Install Ruby 2.7](https://www.ruby-lang.org/en/documentation/installation/)

2. Install dependencies

    ```sh
    bundle
    ```

3. Run development server

    ```sh
    bundle exec jekyll serve
    ```

4. Visit [http://localhost:4000](http://localhost:4000)

5. Make changes to the site!

## Theme Documentation

The site uses the [https://designsystem.digital.gov/](U.S. Web Design System) (USWDS) via [https://github.com/18F/uswds-jekyll](uswds-jekyll). The aim is to maximize use of the system's styles and components, and minimize custom CSS.

### Images

To keep the site loading quickly and friendly to internet connections, images should be resized to be as small as possible while still looking ok.

### Blog Posts

To create a new blog post:

1. Create a file in the format of `YYYY-MM-DD-blog-post-title.md` in the `_posts` folder.
2. The content of the file should match the structure like below:

```markdown
---
layout: post
title: "Introducing Code for Milwaukee"
---

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
```

The body of the post below the `---` can be formatted in [https://guides.github.com/features/mastering-markdown/](Markdown) with text, lists, images, etc.

See this [https://github.com/codeformilwaukee/codeformilwaukee.github.io/pull/16](here) for an example pull request.

### Project Cards

Project cards are listed in a section on the front page with a title, image, short description, and external link to the project. The projects listed must be specified explicitly, but the number isn't limited to 3, and should be relatively flexible.

To add a new project card:

1. Upload an image sized in the ballpark of 275px wide and 175px tall into the `images/projects` folder.
2. Create a new project markdown file located at `_projects/my_project.md`, and fill it out with project information like the example below.

```markdown
---
project_name: Improved Master Property File Data Discovery
image: mprop.jpg
link: https://github.com/codeformilwaukee/breakout-groups/issues/5
---

View and search city property assessment data dynamically!
```

```markdown
---
project_name: Improved Master Property File Data Discovery
image: mprop.jpg
link: https://github.com/codeformilwaukee/breakout-groups/issues/5
---

View and search city property assessment data dynamically!
```

3. Add the project card to the projects section of the home page in `index.md` using the file name in the previous step:
```diff
 <ul class="usa-card-group">
   {% include project-card.html project_slug="mprop" %}
   {% include project-card.html project_slug="WeCountCOVID19" %}
   {% include project-card.html project_slug="decarceration" %}
+  {% include project-card.html project_slug="my_project" %}
 </ul>
```

See [https://github.com/codeformilwaukee/codeformilwaukee.github.io/pull/16](here) for an example pull request of adding a project card.
