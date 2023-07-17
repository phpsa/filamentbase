The source code for the [Filament](https://filamentphp.com) website.

## Contributing

Submitting plugins, tricks, and articles can be done by submitting a pull request to this repository. We have opted for this approach to allow for a more open and transparent process, as well as a smoother review process based on GitHub, where you and Filament maintainers can communicate directly.

### Setting up an author profile

Before you can contribute plugins, tricks or articles to the website, you must set up your author profile. This is then linked to your contributions.

To set up your author profile, create a new file in the `content/authors` directory. The filename should be your name, with spaces replaced by dashes, and the extension should be `.md`. For example, if your name is Dan Harrin, the filename should be `dan-harrin.md`.

```md
---
name: Dan Harrin
slug: dan-harrin
avatar: dan-harrin.jpg
github_url: https://github.com/danharrin
twitter_url: https://twitter.com/danjharrin
---

Your bio should be written in Markdown here. In the future, we may introduce an Author page where people can see your contributions, so feel free to write a little about yourself. Please check the grammar and spelling of this description, preferably using [Grammarly](https://www.grammarly.com). It should be in full sentences.
```

- The `slug` should match the current filename.
- The `avatar` should be the name of a file in the `content/authors/avatars` directory. Your avatar must be square, at least 1000x1000 pixels in size, and preferably a JPEG.
- The `github_url` should be a link to your GitHub profile.
- The `twitter_url` should be a link to your Twitter profile. It is optional.

### Submitting a plugin

To submit a plugin, create a new file in the `content/plugins` directory. The filename should be your author name, followed by the name of your plugin, with spaces replaced by dashes, and the extension should be `.md`. For example, if your author name is "Filament" and the plugin is called "Spatie Media Library", the filename should be `filament-spatie-media-library.md`.

```md
---
name: Spatie Media Library
slug: filament-spatie-media-library
author_slug: filament
categories: [form-builder, form-field, spatie, table-builder, table-column]
description: Filament support for `spatie/laravel-medialibrary`.
discord_url: https://discord.com/channels/883083792112300104/1080807837833384017
docs_url: https://raw.githubusercontent.com/filamentphp/spatie-laravel-media-library-plugin/3.x/README.md
github_repository: filamentphp/spatie-laravel-media-library-plugin
has_dark_theme: true
has_translations: true
image: filament-spatie-media-library.jpg
versions: [2, 3]
---
```

- The `slug` should match the current filename.
- The `author_slug` should match the `slug` of the author profile you created earlier.
- The `categories` should be an array of categories that your plugin is related to. Available categories can be found in the `content/plugin_categories` directory. 
- The `description` should be a short description of your plugin. Please check the grammar and spelling of this description, preferably using [Grammarly](https://www.grammarly.com). It should be one full sentence.
- The `discord_url` should be a link to the Discord channel where people can discuss your plugin. If this doesn't exist yet, you can leave this empty until the Filament team creates it in the official server.
- The `docs_url` should be a URL to a public, raw Markdown file of your plugin. You can leave this blank if your documentation does not live in a raw Markdown file, but please ensure that you have filled in a `url` instead, where we can redirect users who are looking for the documentation.
- The `github_repository` should be the name of the GitHub repository where your plugin is hosted.
- The `has_dark_theme` should be `true` if your plugin supports Tailwind's dark mode, or `false` if not.
- The `has_translations` should be `true` if your plugin supports multiple languages, or `false` if not.
- The `image` should be the name of a file in the `content/plugins/images` directory. The image must fit the 16:9 aspect ratio, at least 2560x1440 pixels in size, and preferably a JPEG. If your image is a screenshot of your plugin, please ensure that it is using a light theme and not a dark theme, to ensure it fits in with the rest of the website.
- The `thumbnail` is optional, and is the name of a file in the `content/plugins/thumbnails directory` directory. The image must fit the 16:9 aspect ratio, at least 2560x1440 pixels in size, and preferably a JPEG. It will be used as a replacement for the `image` any time that the plugin is listed alongside others, and the size is smaller. If you do not provide a `thumbnail`, the `image` will be used instead.
- The `versions` should be an array of Filament major versions that your plugin supports.

#### Quality guidelines

In Filament v2, we introduced the plugins section of the website. We did not enforce many rules on the plugins that were submitted, and as a result, some plugins were not consistent in quality with others. In Filament v3, we are introducing some quality guidelines to ensure that plugins are consistent with each other, and that they are of a high quality. You are more than welcome to create a plugin, distribute it on GitHub and Packagist, and not submit it to the Filament website, if you do not wish to meet these guidelines. However, if you do wish to submit your plugin to the website, please ensure:

- Your plugin's code is hosted on GitHub.
- Your plugin must be available to install from Packagist or [Anystack.sh](https://anystack.sh).
- Documentation should always be public, even if the plugin is paid.
- Documentation should be written clearly, thorough, and well-structured. Users should not be put off from using your plugin because of poor documentation.
- If your plugin contains any UI element, screenshots of any UI should be available in your documentation.

In return for following these guidelines, your plugin will receive free promotion on our website, and a dedicated support channel on our Discord server.

#### Selling a plugin

Filament allows you to sell your plugin on our website. To do this, we've partnered with [Anystack.sh](https://anystack.sh). To get started, visit the `Advertising` section of your Anystack product page, and opt-in to advertising on the `Filament Website`. If you do not follow these instructions, your plugin will not be listed on the website. 15% of sales made through the website will be taken by Filament, to fund the development of the project.

To set up your plugin for sale, you must add an `anystack_id` field to your plugin's Markdown file. You can find "product ID" this from your Anystack product settings.

Please also make sure that `@danharrin` is invited to the private GitHub repository where you are hosting the code, with read-only access. This is to allow us to review your plugin's code.

If you'd like to host your documentation on the Filament website instead of your own, please let us know during the review process, and we can help you get that set up.