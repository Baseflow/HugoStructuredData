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

You might want to add some parameters to your config file as well:

```
title: "Your website title"
baseURL: "https://yourwebsite.com/"
languageCode: "en-us"
languageLang: "en"
defaultContentLanguage: "en"
copyright: "© 2018 Your Company. All rights reserved."

params:
  contact: "hello@yourcompany.com"
  copyright: "© 2018 Your Company. All rights reserved."
  description: "something"
  author: "Your Company"
  env: "production"
  publisher:
    name: "Your Company"
    logo:
      url: "/images/logo.png"
      width: 127
      height: 40
  logo: 
    url: "/images/logo.png"
    width: 127
    height: 40
  image:
    url: "/images/bg.jpg"
    width: 800
    height: 600
  social:
    github: "Your Company"
    facebook: "Your Company"
    facebook_admin: "1111111"  # This needs to be a page admin to get domain insights
    twitter: "Your Company"
    twitter_domain: "yourcompany.com" # This domain shows in twitter cards as "View on `twitter_domain`"
    googleplus: "Your Company"
    pinterest: "Your Company"
    instagram: "Your Company"
    youtube: "Your Company"
    linkedin: "Your Company"
```