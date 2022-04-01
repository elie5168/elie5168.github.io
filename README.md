### Configuration

The [`_config.yml`](_config.yml) file in this repository already contains some variables, you can try to override them in your repository.

### Customizing Head

leaves a placeholder to allow defining custom head, in principle, you can add anything here, e.g. favicons. All you need to do is just creating a file `_includes/custom-head.html` and put data into it.

### Creating Themes

If you want to make your own color schemes, modify the CSS variables in the `_sass/_variables.scss` stylesheet with a scoped data attribute or class name.

For example, below we've created the beginnings of a blue theme:

```scss
// Example blue theme
[data-theme="blue"] {
  --body-bg: var(--blue);
  --body-color: #fff;
}
```

Then, apply the theme by adding `data-theme="blue"` to the `<html>` element.

### Customizing Navigation

You can create a file `_data/navigation.yml` to configure links to some pages. For example,

```yml
- title: Blog
  url: /
- title: About
  url: /about/
```

### Customizing Cover Image

You can set your own cover image by modifying the `cover_image` variable in `_config.yml`, and you can also set different cover images on different pages by setting the `cover_image` variable on each page.

If you discover that the contrast between the cover text color and the cover background color is not enough, you can also adjust these two variables:

```yml
cover_bg_color: rgb(40, 73, 77)
cover_color: rgb(255, 255, 255)
```

### Customizing Social Links

You can set your social links in `_data/social.yml`. You can custom titles, URLs, and icons (only support [Font Awesome](https://fontawesome.com/) currently), for example:

```yml
- title: Email
  url: mailto://eli@gmail.com
  icon: fas fa-envelope
- title: Twitter
  url: https://twitter.com/eli
  icon: fab fa-twitter
- title: GitHub
  url: https://github.com/eli
  icon: fab fa-github
```

### Enabling Posts Archive

Not Pure Poole supports posts archive by date, categories, and tags. For enabling that, you should put some data like below into `_data/archive.yml`:

```yml
- type: dates
  title: Dates
  url: /dates/
- type: categories
  title: Categories
  url: /categories/
- type: tags
  title: Tags
  url: /tags/
```

After that, the navigation to these archive pages would be shown on the top of the homepage.

Then, you can create a category archive page, and set the below parameters on that page:

```yml
---
layout: archive-taxonomies
type: categories
---
```

Or a tag archive page:

```yml
layout: archive-taxonomies
type: tags
```

Or archive by dates:

```yml
layout: archive-dates
```

### Enabling TOC

If you want to show the TOC of a page on the right side, just set `toc: true` on that page.

### Enabling MathJax

If you want to write mathematics on a page, just set `math: true` on that page to enable MathJax.

### Control Grid Width

modify codes in assets/grids-responsive-min.css and default.html

### Search Engine Codes

Codes are placed in home-header.html and sass/_search.scss, and the search engine license is also included in home-header.html

### Development

To set up your environment to develop this theme, run `bundle install`.

Your theme is setup just like a normal Jekyll site! To test your theme, run `bundle exec jekyll serve` and open your browser at `http://localhost:4000`. This starts a Jekyll server using your theme. Add pages, documents, data, etc. like normal to test your theme's contents. As you make modifications to your theme and to your content, your site will regenerate and you should see the changes in the browser after a refresh, just like normal.

When your theme is released, only the files in `_layouts`, `_includes`, `_sass` and `assets` tracked with Git will be bundled.
To add a custom directory to your theme-gem, please edit the regexp in `not-pure-poole.gemspec` accordingly.

### Jekyll theme

Modifications based on Jekyll theme: Not Pure Poole and the previous license is included in index.html file.

### fontawesome

Javascript Version 6.0 and Self-design icon update in default.html.

### License

Open source under the [MIT License](https://opensource.org/licenses/MIT).
