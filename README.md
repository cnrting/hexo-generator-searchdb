# hexo-generator-search

Generate search data for Hexo 3.0. This plugin is used for generating a `search.xml` file, which contains all the neccessary data of your articles that you can use to write a local search engine for your blog.

[Demo](http://wzpan.github.io/hexo-theme-freemind/404.html) - check out the search engine in this 404 page.

## Install

``` bash
$ npm install hexo-generator-searchdb --save
```

## Options

You can configure this plugin in your root `_config.yml`. All the arguments are optional.

``` yaml
search:
  path: search.xml
  field: post
  format: html
  limit: 10000
```

- **path** - file path. Default is `search.xml` .
- **field** - the search scope you want to search, you can chose:
  * **post** (Default) - will only covers all the posts of your blog.
  * **page** - will only covers all the pages of your blog.
  * **all** - will covers all the posts and pages of your blog.
- **format** - the form of the page contents, options are:
  * **html** (Default) - original html string being minified.
  * **raw** - markdown text of each posts or pages.
  * **excerpt** - only collect excerpt.
  * **more** - act as you think.
- **limit** - define the maximum number of posts being indexed, always prefer the newest.