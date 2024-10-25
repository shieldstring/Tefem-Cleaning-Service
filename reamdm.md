CSS (Cascading Style Sheets) is used to control the look and feel of web pages. One of the most powerful features of CSS is selectors, which allow you to target specific elements on a web page to apply styles. Selectors give you the flexibility to control which parts of your HTML get styled, enabling you to create rich, dynamic designs.

In this article, we will explore the basics of CSS selectors, how they work, and the different types of selectors you can use to style specific elements on your webpage.
What Are CSS Selectors?

In CSS, a selector is a pattern that is used to select and target HTML elements that you want to style. Once selected, you can apply various styling rules (like color, font size, background, etc.) to those elements. Selectors are a core concept in CSS because they allow you to pinpoint exactly which elements should be affected by your styles.

For example, in the CSS rule below, p is the selector, which targets all <p> (paragraph) elements in the HTML:

p {
  font-size: 1.2em;
}

Types of CSS Selectors

There are several types of CSS selectors that you can use to target different HTML elements. Let's break down the most common selectors.
1. Type Selectors

A type selector (also known as an element selector) selects all elements of a given type. For instance, if you want to style all paragraphs, all divs, or all heading tags, you would use the type selector.

h1 {
  color: red;
}

2. Class Selectors

A class selector targets elements that have a specific class attribute. Classes are reusable, meaning multiple elements can share the same class.

To use a class selector, you precede the class name with a dot (.):

.my-class {
  background-color: lightblue;
}

In HTML, you apply the class like this:

<div class="my-class">This div has a light blue background.</div>

This rule will apply the background color to all elements with the my-class class, regardless of the element type (whether it's a <div>, <p>, or <span>).

3. ID Selectors

An ID selector targets an element that has a specific id attribute. Unlike classes, an ID should be unique within a page, meaning that only one element should use a specific ID.

To use an ID selector, you precede the ID name with a hash symbol (#):

#header {
  font-size: 24px;
}

In HTML, you apply the ID like this:

<h1 id="header">This is a header</h1>

This rule will only apply to the element with the ID header.
4. Universal Selector

The universal selector targets all elements on a page. It's represented by an asterisk (*).

* {
  margin: 0;
  padding: 0;
}

This rule removes the margin and padding from all elements on the page.

5. Attribute Selectors

An attribute selector allows you to target elements based on the presence or value of a specific attribute.

For example, to select all elements with the type="text" attribute:

input[type="text"] {
  border: 1px solid black;
}

This rule will add a border to all <input> elements that have a type attribute set to text.
6. Descendant Selector

A descendant selector allows you to target an element that is nested inside another element. It is written as two selectors separated by a space.

div p {
  color: green;
}

This rule targets all <p> elements that are inside a <div>.

7. Child Selector

A child selector is similar to a descendant selector but is more specific. It only targets direct children of an element. It's written with a greater-than symbol (>).

div > p {
  color: orange;
}

This rule targets <p> elements that are direct children of a <div>.

8. Adjacent Sibling Selector

The adjacent sibling selector targets an element that is immediately preceded by another element. It is written with a plus sign (+).

h1 + p {
  color: purple;
}

This rule targets the first <p> element that comes directly after an <h1>.

9. General Sibling Selector

The general sibling selector targets all elements that are siblings of a specified element. It is written with a tilde (~).

h1 ~ p {
  color: brown;
}

This rule targets all <p> elements that are siblings of an <h1>.
Pseudo-Class Selectors

10. Pseudo-class selectors allow you to target elements based on their state or position. Common pseudo-classes include:

    :hover: Targets an element when the user hovers over it.
    :nth-child(n): Targets an element based on its position within a parent element.
    :focus: Targets an element when it is focused (e.g., a form input being clicked into).

Example of hover pseudo-class:

button:hover {
  background-color: lightgray;
}

11. Pseudo-Element Selectors

Pseudo-element selectors target specific parts of an element. Common pseudo-elements include:

    ::before: Inserts content before an element.
    ::after: Inserts content after an element.

Example of using ::before to add content:

h1::before {
  content: ">> ";
}
