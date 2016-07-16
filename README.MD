# Building Your First Website
In this workshop you will walk through the steps of building your first website. Before getting started you need to set up our environment and get a basic grasp of the languages that a webpage uses.

## Setting Up Your Environment
To build your website you will need a text editor (a place for you to write the HTML and CSS for your website). As opposed to downloading a text editor, we'll be using c9.io, an online editor, so that you can easily continue developing at home.

## HTML and the Basic Structure of Your Website
HTML stands for Hyper Text Markup Language. To understand what this means let's build the structure for our webpage.

```HTML
<!DOCTYPE html>
<html>
  <head>

  </head>
  <body>

  </body>
</html>
```
Here we see examples of elements and tags. An element is a part of your webpage. In this instance, you have a head, body, and DOCTYPE element. These do not display anything on the page, instead, they help browsers understand further elements in your HTML. Tags help denote elements. Each element has a closing tag, which looks like `<element-name>`, and a closing tag, which looks like `</element-name>`.

Most elements has both a opening and closing tag. If you fail to include both, your page will not display. We see an exception to the rule with the DOCTYPE tag, which serves a unique purpose. The DOCTYPE tag tells the browser what version of HTML the page is written in. Understanding why we use this to denote the version will be a bit convoluted at first, but be sure to include it at the top of every webpage that you create.

The basic structure also includes three other elements: **html**, **head**, and **body**. These elements have both opening and closing tags. The **html** element tells the browser that the page is written in HTML, and represents the root of your webpage. It is meant to be a container for all elements except for the !DOCTYPE.

The **head** denotes the "head" of your HTML page. This is where you will link CSS to your page (which we will discuss more later), include **meta** tags to covey information to search engines, and set the title for your webpage. Let's do that now. In your head tags add a **title** tag.

```HTML
<!DOCTYPE html>
<html>
  <head>
    <title></title>
  </head>
  ...
```

Notice how the **head** and **body** tags are multiline, whereas the **title** tag is only single line. Generally, elements that can include other elements inside them are multiline. Because both the **head** tag and the **body** tag can include other tags within them, they are multiline tags. Let's put some text within our title tag.

```HTML
  ...
  <head>
    <title>Steven's Website</title>
  </head>
  ...
```

The text within the **title** tag doesn't display directly on the page. It displays on the tab of your website, at the very top of your browser.
