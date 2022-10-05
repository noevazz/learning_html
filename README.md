# HTML

The Hypertext Markup Language defines the **structure** of a web page.
It enclose the contents of the page inside **elements** which have a significant meaning for the browser.

![html_css_js.png](./media/html_css_js.png)

> HTML is not a programming language, it is a Markup language.

## Elements and Tags

Elements are enclose content between **tags**.

Tags are the starting and ending parts of an element.

For example the **p** element defines a paragraph. The starting tag for this element is `<p>` and the ending tag is `</p>`.

Then you can put content between this tags:

```html
<p>Hello this is a paragraph</p>
```

> See example above at [codes/paragraph.html](./codes/paragraph.html)

As you can see ending tags are almost equals to the starting tag, the only difference is that ending tags have a forward slash `/`.

## Attributes

Elements can have attributes that give a bit extra info to the browser.

Example, the `a` tag is used to create a link:

```html
<a href="https://www.google.com/">click to go google</a>
```

> See example above at [codes/anchor.html](./codes/anchor.html)

> Attributes must be in the starting tag, **never** in the ending tag.

As you can see, the `href` (hyper reference) attribute is used in `a` elements to provide the link we want to use. Note that the value of the attribute is enclosed between quotes, you can also use simple quotes but do not mix both.

There are some attributes that are common in the majority of elements, and other attributes that are reserved for specific elements, you will learn more attributes and elements later on this course.

## Unclosed tags

Jus a few elements does not need and ending tag. You will learn some of them throughout this course.

Unclosed tags does not have content that's why an ending tag is not needed.

> Unclosed tags are also known as  self closing tags, void tags, empty tags, singletons tags.

Examples are:

- `<img />` for images
- `<br />` to insert a single line break
- `<hr />` to add a horizontal rule

> `br`and `hr`are example of empty tags because you rarely will add an attributes to them, you just use them as they are.

> Also note there is an space between the tag and the slash, older web browsers will have issues to understand this, therefore try to add that space.

Although you can use a slash ath the end of the tag `/>` this is not mandatory and does not give any special meaning to the browser.

The browser will remove the slashes and then render the elements:

![unclosed_tags.png](./media/unclosed_tags.png)

> You can see the code of the image at [codes/unclosed_tags.html](./codes/unclosed_tags.html)

HOWEVER, for XHTML (a similar language but more strict) it is required to add that slash in unclosed tags. ALSO some frameworks like **react** will trow an error if these are not closed.

📌 **Good practice**: ALWAYS "close" an unclosed tag by adding a slash at the end.

## DOCTYPE declaration

The `Doctype` declaration is an "information" to the browser about the HTML version. We can also refer to the Doctype as the **Document Type Declaration** (DTD)  

**It is NOT a tag**

that is used to specify the HTML version.

It must appear at the beginning of an HTML file. For HTML5 the syntax is a follows:

```html
<!DOCTYPE html>
```

> The Doctype declaration is NOT case sensitive, so it is not mandatory to use all letters is upper case.

## HTML tag

The `HTML` represents the root of an HTML document. It is a container for all other elements, except for the DOCTYPE.

Example:

```html
<!DOCTYPE html>
<html>
</html>
```

## Head tag

The `head` tag is used to group information about the document, e.g. title, character encoding, icon of the tab, useful metadata, etc.

Example:

```html
<!DOCTYPE html>
<html>
    <head>
    </head>
</html>
```

Let's add some elements to the `head`:

```html
<!DOCTYPE html>
<html>
    <head>
        <title>My page</title>
        <meta charset="UTF-8">
    </head>
    <p>I am not inside the head tag. México.</p>
</html>
```

> See example above at [codes/head_tag.html](./codes/head_tag.html)

This is how it looks in the browser:

![head_tag.png](./media/head_tag.png)

- Note the name of the tab, that was caused by the `title` tag. This tag is important for Search Engine Optimization (SEO).
- Note the `é` in `México`, we were able to see that symbol because we use `<meta charset="UTF-8">`, the `meta` tag defines metadata, in can have multiple attributes, this time we use `charset` to set the character encoding to `UTF-8` so we can see the letter `é`.

## Body tag

The `body` tag defines the document's body, it contains all the HTML elements e.g. paragraphs, links, images, tables, etc.

> Note: Only use the `body` element once in your document.

Example:

```html
<!DOCTYPE html>
<html>
    <head>
        <title>My page</title>
        <meta charset="UTF-8">
    </head>
    <body>
        <h1>This is my page<h2>
        <p>I am not inside the head tag. México.</p>
        <h2>Hello World</h2>
    </body>
</html>
```

> See example above at [codes/body_tag.html](./codes/body_tag.html)

This is how it looks in the browser:

![body_tag.png](./media/body_tag.png)

- The `h1` tag is used to add a heading, there are 6 levels for headings: `h1`, `h2`, `h3`, `h4`, `h5`, and `h6`, each heading represents the level of importance, being `h1` the most important heading. This is important for SEO.

## More about links

We already se the `a` element is used to redirect a user when the link is clicked.

This element can have a few attributes:

- `href`: (optional, but makes no sense to use the `a` element if you are not going to redirect at all) The link where we want to redirect the user.
- `title`: (optional) an small message the user will se when hovering the pointer over the link.
- `target`: (optional) specifies where to open the link, values:
    - `_blank`: Opens the linked document in a new window or tab
    - `_self`: Opens the linked document in the same frame as it was clicked (this is default)
    - `_parent`: Opens the linked document in the parent frame
    - `_top`: Opens the linked document in the full body of the window
    - `framename`: Opens the linked document in the named iframe

Example:

```html
<!DOCTYPE html>
<html>
  <head> </head>
  <body>
    <a
      href="https://www.facebook.com/"
      title="click here to open facebook"
      target="_blank"
      >Go to facebook</a
    >
  </body>
</html>
```

> See example above at [codes/more_about_anchor.html](./codes/more_about_anchor.html)

This is how it looks in the browser:

![body_tag.png](./media/more_about_anchor.png)

> The cursor is not shown in the screenshot but the message was shown when the user hover pointer over the link.