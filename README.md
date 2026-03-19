# Phantom

This is a [Statiq Web](https://statiq.dev/web) blogging theme based on the [Phantom](https://html5up.net/phantom) template by [HTML5 UP](https://html5up.net), adapted from the [Wyam Phantom theme](https://github.com/Wyamio/Wyam/tree/develop/themes/Blog/Phantom) using [CleanBlog](https://github.com/statiqdev/CleanBlog) as a structural template.

## Minimum Statiq Web Version

This theme requires Statiq Web 1.0.0-beta.36 or later.

## Installation

Statiq themes go in a `theme` folder alongside your `input` folder. If your site is inside a git repository, you can add the theme as a git submodule:

```
git submodule add https://github.com/AlexHedley/Phantom.git theme
```

Alternatively, you can clone the theme directly:

```
git clone https://github.com/AlexHedley/Phantom.git theme
```

Once inside the `theme` folder, Statiq will automatically recognize the theme.

## Site Contents

### Blog Posts

Add your blog posts to a `posts` folder under your own `input` folder. An example post might be named `input/posts/example.md` and contain the following content:

```
Title: This Is An Example Post
Lead: Yay for examples!
Published: 2024-01-01
Tags:
  - Examples
  - Tag with spaces
---
This is my example blog post content.
```

### Static Pages

Add your static pages to a `pages` folder under your own `input` folder. An example page might be named `input/pages/about.md`.

```
NavbarTitle: About
Order: 1
Title: About me
---
Hi there!
```

## Customization

### Basic Configuration

Create a `settings.yml` file in your site root:

```yaml
Host: yourdomain.github.io
LinksUseHttps: true

SiteTitle: My Phantom Blog
SiteDescription: A blog about things
Copyright: => $"All content © {DateTime.Now.Year} Your Name"
```

## Settings

### Global

- `SiteTitle`: The title of the site (shown in the logo/header).
- `SiteDescription`: The subtitle shown on the home (index) page.
- `PostSources`: A globbing pattern where to find blog posts (defaults to `posts/**/*`).
- `PageSources`: A globbing pattern where to find static pages (defaults to `pages/**/*`).

### Page

- `Title`: The title of the page (or post).
- `NavbarTitle`: The title of the page to use in the navigation menu (optional, `Title` will be used if not specified).
- `Description`: A description of the page.
- `Lead`: Descriptive text that expands on the title of a post.
- `Tags`: Tags for a blog post.
- `Published`: The date a page or post was published.
- `Image`: Path to an image for the page or post (displayed as a full-width image below the header).
- `ShowInNavbar`: Set to `false` to hide a static page in the navigation menu.
- `IsPost`: Set to `false` to exclude the file from the set of posts.
- `IsPage`: Set to `false` to exclude the file from the set of static pages.

### Post Comments

- `CommentEngine`: The comment engine to use for posts (empty string or "none" to disable comments).

Currently, the only available comment engine is [giscus](https://giscus.app).

#### Giscus

The following settings must be set in your `settings.yml` when `CommentEngine` is set to `giscus`:

- `GiscusRepoName`: Name of the repository whose discussions act as storage.
- `GiscusRepoId`: ID of the repository.
- `GiscusCategoryId`: ID of the discussion category.

## Partials

Replace or copy any of these Razor partials in your `input` folder to override sections of the site:

- `/_head.cshtml`: Additional content for the `<head>` tag.
- `/_navigation.cshtml`: The navigation header and sidebar menu.
- `/_navbar.cshtml`: The items in the navigation menu.
- `/_header.cshtml`: The header section of the page.
- `/_posts.cshtml`: Displays a set of posts.
- `/_post.cshtml`: Displays an individual post inside a list of posts.
- `/_post-after-content.cshtml`: Displays content at the bottom of a post, before comments.
- `/_page-after-content.cshtml`: Displays content at the bottom of a static page.
- `/_common-after-content.cshtml`: Displays content at the bottom of any page.
- `/_copyright.cshtml`: Displays copyright in the footer.
- `/_post-comments.cshtml`: Displays comments for a post.
- `/_post-comments-{engine}.cshtml`: Displays the comment engine partial.
- `/_sidebar.cshtml`: Additional sidebar content on the home page.
- `/_scripts.cshtml`: Additional scripts at the bottom of each page.
- `/_footer.cshtml`: The footer section.

## Credits

- Phantom theme by [HTML5 UP](https://html5up.net) (CCA 3.0 license)
- Originally adapted for Wyam by the [Wyam project](https://github.com/Wyamio/Wyam)
- Structured for Statiq using [CleanBlog](https://github.com/statiqdev/CleanBlog) as a template
