# Draft

Draft is a PHP Static Site Generator.

## Why the name Draft?
From the time I heard about [reactphp](https://reactphp.org/) I wanted to work with it. But there was not any sort of starter template or framework to take it up.
With [DriftPhp](https://driftphp.io/), I finally found something to get started. Since this is a draft generator of sort which generates drafts of blog posts and it is close to Drift. 
Hence, Draft.


### Installation

`composer create-project draftphp/draft`

### Development

`php draft dev`

This runs a development server at `http://localhost:8888`.

### Folder Structure

#### /pages
This is where all the pages for the site lives

#### /layouts
This is where all the layouts for the site lives

#### /assets
This is where the images live

Note: All of these can be changed here in the [/config.php](/config.php).

### `<draft>`
We include 'meta' for post in a `<draft>` tag. Meta here means whatever you want to be replaced in the content of the page.

> `{content}` in the layout and `layout` in the `<draft>` tag are reserved and cannot be used to replace the contents in the page

The syntax in the template is `{meta}`.
For example if you want to add title to a page `{title}`, add a 
```
title: This is the test title
```
in your draft tag. 
and in your layout. You would add

```html
...
<title>{title}</title>
...

```

This will generate 
```html
<title>This is the test title</title>
```
in the HTML.
  
Example draft tag
```
<draft>       
    description: this is the best description
    title: This is the test title
    layout: blog.html
</draft>
``` 
