# Building Your First Website
In this workshop you will walk through the steps of building your first website. Before getting started we need to set up our environment and get a basic grasp of the languages that a webpage uses.

## Setting Up Your Environment
To build your website you will need a text editor (a place for you to write the HTML and CSS for your website). As opposed to downloading a text editor, we'll be using c9.io, an online editor, so that you can easily continue developing at home.

## Setting Up File Structure


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
Here we see examples of elements and tags. An element is a part of your webpage. In this instance, you have a head, body, and DOCTYPE element. These do not display anything on the page, instead, they help browsers understand further elements in your HTML. Tags help denote elements. Each element has an opening tag, which looks like `<element-name>`, and a closing tag, which looks like `</element-name>`.

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
    <title>Your First Website!</title>
  </head>
  ...
```

The text within the **title** tag doesn't display directly on the page. It displays on the tab of your website, at the very top of your browser.

## Headings and Paragraphs
Let's continue building out site, we'll learn more about the the different parts of HTML as we continue. Now let's add some visible content on our site. First we'll add a heading tag within the body tags of our site.

```HTML
  ...
  <body>
    <h1>Hello World!</h1>
  </body>
  ...
```

Heading tags go from **h1** to **h6**, in order of largest to smallest. This is one way we can display text, another way is through the **p** tag, or the paragraph tag. Let's also add a paragraph tag to the site.

```HTML
  ...
    <h1>Hello World!</h1>
    <p>Hello Again!</p>
  </body>
  ...
```

Now let's reload our web page and view the result. As you can see, the site is displaying both a paragraph tag and a heading tag. Heading tags should only be used as the name suggests, like headings.

## Lists
Let's add lists to our HTML page. There are two types of lists, ordered lists (numbered lists) and unordered lists (bulleted lists). Let's go into our **body** and add both kinds of lists.

```HTML
  ...
    <p>Hello Again!</p>
    <ol>
      <li>Item 1</li>
      <li>Item 2</li>
      <li>Item 3</li>
    </ol>
    <ul>
      <li>Item A</li>
      <li>Item B</li>
      <li>Item C</li>
    </ul>
  </body>
  ...
```

The **ol** tag stands for ordered list, whereas the **ul** tag stands for unordered list. The **li** tag is simply a list element. Let's save and reload our webpage to see the result.

## Navigation
```HTML
  ...
  <body>
    <nav>
			<a href="index.html">Index</a>
			<a href="about.html">About</a>
		</nav>
  ...
```

## Divisions (Divs)
```HTML
  ...
  </nav>

  <div class="segment">
    <h1 class="title">Hello World!</h1>
  </div>
```

## Images
```HTML
  ...
  <div class="segment">
    <p id="imgheading">Pupper</p>
    <img src="https://www.rover.com/blog/wp-content/uploads/2014/07/dog-dance-funny.gif" alt="Dog dancing" width="30%">
  </div>
```

## Linking our HTML and CSS
Great! We’ve finished the HTML for our site, but it looks bland. Let’s go back in and style the website with CSS. We’ll talk more about what CSS is later on, let’s first add a link in our HTML.

Go back to the head, which should only contain a **title** tag. Underneath it let’s add a **link** tag.

```HTML
  ...
  <head>
    <title>Your First Website!</title>
    <link>
  </head>
  ...
```

The link element is a unique, there is no closing tag. As the name suggests, it's used to link to another file. However, we do not use this to display links. To display links we use the **a** tag, which we learned about earlier.

Our **link** tag also needs the **rel** attribute and the *href* attribute. The **rel** attribute stands for relation, it specifies the relation between the *link* tag and the **href** attribute. In this instance, the link is referencing a stylesheet, which is why the value of **rel** is **stylesheet**.

Now we need to specify the file we’re accessing. Let’s go into our file structure and create a folder for our CSS files, called `styles`. In that folder add a `main.css` file, which will contain our CSS for both the `index.html` and the `about.html`.

```HTML
  My Website
  |- index.html
  |- about.html
  |
  |- styles
      |- main.css
```

Now, let’s go into back to our **link** tag and connect the CSS to our HTML. After the **href** attribute, add the file path for `main.css`. Since the file is located in the styles folder, the value of our path should read 'styles/main.css'. Our link tag should now look like this:

```HTML
  ...
    <link rel=”stylesheet” href=”styles/main.css”>
  </head>
  ...
```

To ensure that our site is working, let’s go into our CSS file and change the background color to red. We’ll talk more about the syntax of the code we’re about to write later on.

```CSS
  h1 {
    background-color: red;
  }
```

Save both your `index.html` and your `main.css` and reload your website. If your webpage has turned an ugly shade of red, congrats! You’ve successfully linked your CSS file to your HTML.

Now we’re ready to make our website look nice, but first we need to understand the basics of CSS.

##Styling Your HTML with CSS
CSS stands for Cascading Style Sheets. Once you create the basic structure of your web page, you can use CSS to change the way it looks.

There are three types of css attributes we will be working with: elements, classes, and ids. Elements in css correspond to their HTML counterparts of the same name. Making changes to an element will affect all elements of that name. Classes are used in css when you want to change more than one of an element, but not all of them. Ids are used in css when you only want to change a single element. Making changes to a class or id will only change elements that have that class or id.

To assign an element with a class or id, open your HTML file and simply type `class=”classname"` or `id=”idname”` into the opening tag like this:

```HTML
  …
  <div class=”classname”>
    …
  </div>
  …
```

CSS code is organized in blocks referring to a specific attribute. For example, to change the **h1** tag we must first create a block of css code that looks like this:

```CSS
  …
  h1 {
    …
  }
  …

```

Now that we have a block of code for the **h1** tag, we can change the font. But first, we have to import the font into our website.

Go to https://www.google.com/fonts#UsePlace:use/Collection:Lato and select the Normal 400, Normal 400 Italic, and Bold 700 options. While selecting everything will increase your options, it will also affect website load time. So only select what you’re going to use!

Next, scroll down to the section that says “3. Add this code to your website”. Press the @important tab and copy the code.

Open your `styles.css` file in your text editor and paste the code into the document. This imports the font and allows you to use in your web page. Now we can add the font to our elements.
