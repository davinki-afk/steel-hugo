---
title: "Header and footer configuration"
date: 2026-08-16
author: "Author name"
description: "Guide to configuring the website header and footer."
tags: ["Hugo", "toml"]
categories: ["Guide", "Blog"]
---
# Header
## Title and subtitle
The site title is edited directly via the first line of **hugo.toml**. To configure the site slogan, navigate to the **[language]** section, then locate the desired language and the **subtitle** parameter. For example:
```toml
[languages.en.params]
    subtitle = "A tabular, compact theme for Hugo."
```

## Menu
Menu settings are still located under the **[language]** item. Example of configuring a menu item in the header:

```toml
[[languages.en.menus.main]] # Creating a new menu item in a specific language (e.g., EN)
    name = "Home" # Display name
    pageRef = "/" # Link
    weight = 10 # Regarding the point's position: the greater the weight, the further to the right it will be, and vice versa.
```
To create a menu item in another language, change the language code.

# Footer
## Copyright
To change the copyright text, go back to **[language]**, find the **copyright** parameter and change the default text to the desired one.
```toml
[languages.en.params]
    copyright = "Name and surname; all rights reserved, subject to the first amendment to the agreement."
```
## Menu
To create a menu column, go to the **[language]** section and insert the following parameters:
```toml
[[languages.en.params.footerColumns]] # Creates a new column
    title = "Column Example" # Column title
    [[languages.en.params.footerColumns.links]] # Creates a new item in the column
        name = "Link" # Item name
        url = "/link/" # Link
```
To add a new item in the same column, copy the item's parameters and paste them into the same column.