# after-rust

![after-rust screenshot](https://github.com/vms20591/after-rust/blob/master/screenshot.png?raw=true)

This template is based on [after-dark](https://github.com/getzola/after-dark.git) template. The changes are purely style based as of now. Leaving original instructions below.

---

## after-dark

![after-dark screenshot](https://github.com/getzola/after-dark/blob/master/screenshot.png?raw=true)

### Contents

- [Installation](#installation)
- [Options](#options)
  - [Top menu](#top-menu)
  - [Title](#title)

#### Installation
First download this theme to your `themes` directory:

```bash
$ cd themes
$ git clone https://github.com/getzola/after-dark.git
```
and then enable it in your `config.toml`:

```toml
theme = "after-dark"
```

This theme requires your index section (`content/_index.md`) to be paginated to work:

```toml
paginate_by = 5
```

The posts should therefore be in directly under the `content` folder.

The theme requires tags and categories taxonomies to be enabled in your `config.toml`:

```toml
taxonomies = [
    # You can enable/disable RSS
    {name = "categories", rss = true},
    {name = "tags", rss = true},
]
```
If you want to paginate taxonomies pages, you will need to overwrite the templates
as it only works for non-paginated taxonomies by default.


### Options

#### Top-menu
Set a field in `extra` with a key of `after_dark_menu`:

```toml
after_dark_menu = [
    {url = "$BASE_URL", name = "Home"},
    {url = "$BASE_URL/categories", name = "Categories"},
    {url = "$BASE_URL/tags", name = "Tags"},
    {url = "https://google.com", name = "Google"},
]
```

If you put `$BASE_URL` in a url, it will automatically be replaced by the actual
site URL.

#### Title
The site title is shown on the homepage. As it might be different from the `<title>`
element that the `title` field in the config represents, you can set the `after_dark_title`
instead.

### Original
This template is based on the Hugo template https://git.habd.as/comfusion/after-dark
