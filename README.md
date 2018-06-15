# HugoStructuredData
 Collection of structured data snippets in Google preferred JSON-LD format, with support for Hugo.

Based on the work of: https://github.com/JayHoltslander/Structured-Data-JSON-LD

# Usage

Copy the `schemas` folder into your partials folder.

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

You should add the paramters that are in the `config.metadata.yaml` file into your config file as well. You could also use that file as second config directly.