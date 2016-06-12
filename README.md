# update

2015.12.05 add a pr to the base line:

1. fix a markdown format display issue
2. fix the unicode tilte issue that will has wrong url and not be routed.

# WordPress to Hugo Exporter

Hugo a static site generator written in GoLang: [http://hugo.spf13.com/](http://hugo.spf13.com/)

This repo is based on [https://github.com/benbalter/wordpress-to-jekyll-exporter](https://github.com/benbalter/wordpress-to-jekyll-exporter)

### Changes

- mainly for the front matter section
- renamed jekyll to hugo

## Hugo Features

One-click WordPress plugin that converts all posts, pages, taxonomies, metadata, and settings to Markdown and YAML which can be dropped into Hugo.

## Features

* Converts all posts, pages, and settings from WordPress for use in Hugo
* Export what your users see, not what the database stores (runs post content through `the_content` filter prior to export, allowing third-party plugins to modify the output)
* Converts all `post_content` to Markdown Extra (using Markdownify)
* Converts all `post_meta` and fields within the `wp_posts` table to YAML front matter for parsing by Hugo
* Generates a `config.yaml` with all settings in the `wp_options` table
* Outputs a single zip file with `config.yaml`, pages, and `post` folder containing `.md` files for each post in the proper Hugo naming convention
* No settings. Just a single click.

## Usage

1. Place plugin in `/wp-content/plugins/` folder
2. Make sure `extension=zip.so` line is uncommented in your `php.ini`
3. Activate plugin in WordPress dashboard
4. Select `Export to Hugo` from the `Tools` menu

## Command-line Usage

If you're having trouble with your web server timing out before the export is complete, or if you just like terminal better, you may enjoy the command-line tool.

It works just like the plugin, but produces the zipfile at `/tmp/wp-hugo.zip`:

    php hugo-export-cli.php

Alternatively, if you have [WP-CLI](http://wp-cli.org) installed, you can run:

```
wp hugo-export > export.zip
```

The WP-CLI version will provide greater compatibility for alternate WordPress environments, such as when `wp-content` isn't in the usual location.

## License

The project is licensed under the GPLv3 or later

