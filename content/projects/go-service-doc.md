+++
title = "go-service-doc"
date = "2022-01-19"
author = "Fredrik"
description = "This is a tool to generate a static web site based on Markdown files."
+++

This is a tool to generate a static web site based on Markdown files.

[Link to the project.](https://github.com/lonnblad/go-service-doc)

It will:

- convert Markdown files to HTML pages ([more info](#html-page-generator))
- generate a menu based on `#` and `##` headers ([more info](#side-menu-generator))
- add styling similar to what is used by github to display Markdown files

go-service-doc also supports embedding static files, [more info](#embedding-images).

You can find a list of all features [here](#features)

go-service-doc will generate both HTML files to be deployed standalone and a `go` handler, which could be used in your service.
Here you can find a [deployed example](https://lonnblad.github.io/go-service-doc) of the generated HTML files.
