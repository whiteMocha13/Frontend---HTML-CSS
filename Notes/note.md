## Html_Css Notes 

---
#### Inline vs Block-Level Elements 

Most elements are either block- or inline-level elements. What’s the difference?

Block-level elements begin on a new line, stacking one on top of the other, and occupy any available width. Block-level elements may be nested inside one another and may wrap inline-level elements. We’ll most commonly see block-level elements used for larger pieces of content, such as paragraphs.

Inline-level elements do not begin on a new line. They fall into the normal flow of a document, lining up one after the other, and only maintain the width of their content. Inline-level elements may be nested inside one another; however, they cannot wrap block-level elements. We’ll usually see inline-level elements with smaller pieces of content, such as a few words.

Both `<div>` s and `<span>`s, however, are extremely valuable when building a website in that they give us the ability to apply targeted styles to a contained set of content.

A `<div>` is a block-level element that is commonly used to identify large groupings of content, and which helps to build a web page’s layout and design. A `<span>`, on the other hand, is an inline-level element commonly used to identify smaller groupings of text within a block-level element.

We’ll commonly see `<div>`s and `<span>`s with class or id attributes for styling purposes. Choosing a class or id attribute value, or name, requires a bit of care. We want to choose a value that refers to the content of an element, not necessarily the appearance of an element.

---

#### Structural Elements 

For the longest time the structure of a web page was built using divisions. The problem was that divisions provide no semantic value, and it was fairly difficult to determine the intention of these divisions. Fortunately HTML5 introduced new structurally based elements, including the `<header>`, `<nav>`, `<article>`, `<section>`, `<aside>`, and `<footer>` elements.

All of these new elements are intended to give meaning to the organization of our pages and improve our structural semantics. They are all block-level elements and do not have any implied position or style. Additionally, all of these elements may be used multiple times per page, so long as each use reflects the proper semantic meaning.

The `<nav>` element identifies a section of major navigational links on a page. The `<nav>` element should be reserved for primary navigation sections only, such as global navigation, a table of contents, previous/next links, or other noteworthy groups of navigational links.

The `<article>` element is used to identify a section of independent, self-contained content that may be independently distributed or reused. We’ll often use the `<article>` element to mark up blog posts, newspaper articles, user-submitted content, and the like.
When deciding whether to use the `<article>` element, we must determine if the content within the element could be replicated elsewhere without any confusion. If the content within the `<article>` element were removed from the context of the page and placed, for example, within an email or printed work, that content should still make sense.

The `<section>` element is used to identify a thematic grouping of content, which generally, but not always, includes a heading. The grouping of content within the `<section>` element may be generic in nature, but it’s useful to identify all of the content as related.

The `<aside>` element holds content, such as sidebars, inserts, or brief explanations, that is tangentially related to the content surrounding it. When used within an `<article>` element, for example, the `<aside>` element may identify content related to the author of the article.
We may instinctively think of an `<aside>` element as an element that appears off to the left or right side of a page. We have to remember, though, that all of the structural elements, including the `<aside>` element, are block-level elements and as such will appear on a new line, occupying the full available width of the page or of the element they are nested within, also known as their parent element.

The `<aside>` element holds content, such as sidebars, inserts, or brief explanations, that is tangentially related to the content surrounding it. When used within an `<article>` element, for example, the `<aside>` element may identify content related to the author of the article.

We may instinctively think of an `<aside>` element as an element that appears off to the left or right side of a page. We have to remember, though, that all of the structural elements, including the `<aside>` element, are block-level elements and as such will appear on a new line, occupying the full available width of the page or of the element they are nested within, also known as their parent element.

---

#### Encoding Special Characters

```html
<footer>
  <small>&copy; Styles Conference</small>
</footer>
```

The `<h3>` element within our `<header>` element, as well as the `<small>` element within our `<footer>` element, has some interesting things going on. Specifically, a few special characters within these elements are being encoded.

Special characters include various punctuation marks, accented letters, and symbols. When typed directly into HTML, they can be misunderstood or mistaken for the wrong character; thus they need to be encoded.

Each encoded character will begin with an ampersand, &, and end with a semicolon, ;. What falls between the ampersand and semicolon is a character’s unique encoding, be it a name or numeric encoding.

For example, we would encode the word “resumé” as resum&eacute;. Within our header we have encoded both en and em dashes, and within our footer we have encoded the copyright symbol. For reference, a long list of character encodings may be found at Copy Paste Character.

---

#### Linking to an Email Address

Occasionally we may want to create a hyperlink to our email address—for example, hyperlink text that says “Email Me,” which when clicked opens a user’s default email client and pre-populates part of an email. At a minimum the email address to which the email is being sent is populated; other information such as a subject line and body text may also be included.
To create an email link, the href attribute value needs to start with mailto: followed by the email address to which the email should be sent. To create an email link to shay@awesome.com, for example, the href attribute value would be mailto:shay@awesome.com.

```html
<a href="mailto:shay@awesome.com?subject=Reaching%20Out&body=How%20are%20you">Email Me</a>
```

Additionally, subject, body text, and other information for the email may be populated. To add a subject line, we’ll include the subject= parameter after the email address. The first parameter following the email address must begin with a question mark, ?, to bind it to the hyperlink path. Multiple words within a subject line require that spaces be encoded using %20.
Adding body text works in the same way as adding the subject, this time using the body= parameter in the href attribute value. Because we are binding one parameter to another we need to use the ampersand, &, to separate the two. As with the subject, spaces must be encoded using %20, and line breaks must be encoded using %0A.
Altogether, a link to shay@awesome.com with the subject of “Reaching Out” and body text of “How are you” would require an href attribute value of `mailto:shay@awesome.com?subject=Reaching%20Out&body=How%20are%20you`.

---
