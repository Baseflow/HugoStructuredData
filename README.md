# HugoStructuredData
 Collection of structured data snippets in Google preferred JSON-LD format, with support for Hugo.

Based on the work of: https://github.com/JayHoltslander/Structured-Data-JSON-LD

This uses the [Hugo pipelines](https://gohugo.io/themes/theme-components/) introduced in [Hugo 0.42](https://gohugo.io/news/0.42-relnotes/)

# Usage

Start by adding this theme to your website in the config file:

```
theme:
- your-own-theme
- structured-data
- some-other-theme
```

Change the properties inside `themes/structured-data/config.yaml` to match you details.

Add this snippet to the `<head>` of your baseof.html

`{{ partial "schemas/schema_Global.html" . }}`

Add `contenttypes` to the parameters of the pages you would like to include the schemes in.

```
---
title: "Some person"
date: 2018-03-28T21:58:30+02:00
contenttypes: ["Person"]
---
```

Or another example

```
---
title: "This is a blog and article"
date: 2018-03-28T21:58:30+02:00
contenttypes: ["BlogPosting, "Article"]
---
```

Other available properties are:

```
---
type: blog
layout: post
title: "Introducing blog"
date: 2018-06-01T16:40:55+01:00
author: notmartijn
contenttypes: ["BlogPosting"]
---
```

In this case the author of the file will be `notmartijn` instead of the default author `martijn`.

To add, change or remove locations or authors look in the data folder.