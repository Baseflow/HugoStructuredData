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

Add the folowing parameters to your config file:

```
params:
  name: "YourName" # your company name
  contact: "hello@yourname.com" # Primary email address
  phone: "0123345678" # Primary phone
  copyright: "© 2018 YourName. All rights reserved."
  description: "YourName" # Add a short description
  logourl: "images/logo.png" # Used in structured data as logo url
  imageurl: "images/bg.jpg" # Used in structured data as background image
  pricerange: "$$" # Used in structured data as price range
  primarylocation: "enschede" # Used as primary location if no specific is set
  primaryauthor: "martijn" # Used as primary author if no specific is set
  keywords: ["mobile", "web", "ai", "backend", "open source"] # Can be overriden per page
  social:
    website: "https://yourwebsite.com"
    github: "YourName"
    facebook: "YourName"
    facebook_admin: "1111111"  # This needs to be a page admin to get domain insights
    twitter: "YourName"
    twitter_domain: "yourname.com" # This domain shows in twitter cards as "View on `twitter_domain`"
    googleplus: "YourName"
    pinterest: "YourName"
    instagram: "YourName"
    youtube: "YourName"
    linkedin: "YourName"
  images:
    ["images/bg.jpg"] # For twitter cards
```

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

To add, change or remove locations or authors look in the data folder.