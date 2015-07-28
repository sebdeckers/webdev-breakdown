# Web Development: Let's Break it Down
[![Join the chat at https://gitter.im/SingaporeJS/discussion](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/SingaporeJS/discussions)

## Development Tools
Web browsers come with built-in developer tools.
- [Google Chrome](https://www.google.com/chrome/browser/desktop/) right-click on any web page and inspect element

Online code editors for prototyping, demos, experiments, hacks.
- [Codepen](http://codepen.io/)

Local editors to build larger apps and sites with code across multiple files.
- [Atom](https://atom.io/)

Version Control Systems record changes to source files. Useful when building applications over time or with collaborators.
- Git is bundled with the GitHub App for [Windows](https://windows.github.com/) or [Mac](https://mac.github.com/)

Code hosting makes it easy to share code with others. These also come with collaboration tools: branches, pull requests, & issues.
- [GitHub](https://github.com/)

Web pages are hosted on a web server. These are computers that are always on and available via a public domain name.
- [GitHub Pages](https://pages.github.com/)
- [Heroku](https://www.heroku.com/)

## HTML
Web pages are written in Hyper Text Markup Language, abbreviated as HTML. This HTML code contains the text content of the page.

Other files can be references, such as images or videos.

```html
<!doctype html>
<html>
  <head>
    <title>Easy does it</title>
  </head>
  <body>
    This is a totally legit web page.
  </body>
</html>
```

HTML adds structure to the content, like titles, sections, footers, etc. This code is called a tag. Most tags have and an opening and a closing surrounding their text content. Tags can also have attributes that contain extra information for the browser.

```html
<!-- This is a comment and will be ignored by the browser.
     These tags all go into the <body> content. -->
<h1>Here's a pretty important header.</h1>
<p>This is a paragraph of text.</p>
<a href="https://ninja.sg/">I am a link.</a>
<img src="http://i.imgur.com/qLfZ9BO.jpg" alt="Helicopter dog">
<iframe width="560" height="315" src="https://www.youtube.com/embed/3MteSlpxCpo"></iframe>
```

## CSS
Adding design and layout to web pages is done using Cascading Style Sheets, aka CSS. This is a different language better suited to describe what the HTML elements should look like.

```css
/* CSS code can also contain comments.
   They use a slightly different syntax from HTML comments,
   but are similarly inert. */
h1 {
  text-align: center;
  font-family: serif;
  font-size: 28px;
}
p {
  font-family: sans-serif;
  font-size: 14pt;
}
a {
  text-decoration: underline;
  color: blue;
}
img {
  border: 5px solid gold;
  width: 50%;
  height: 50%;
  transition: border-color 1s;
}
img:hover {
  border-color: skyblue;
}
```
There are several ways to apply CSS code to an HTML document.
1. Referenced with a `<link>` tag.
  ```html
  <link rel='stylesheet' href='example.css'>
  ```
1. Embedded within a `<style>` tag.
  ```html
  <style>
    header { color: orange }
  </style>
  ```
1. Inline with the `style` attribute on any HTML tag.
  ```html
  <p style='background: wheat'></p>
  ```

## JavaScript
Interactive behaviour of the web page content is coded in JavaScript. The browser offers many ways to manipulate the web page.
```js
document.query('button')
  .addEventListener('click', event => {
    window.alert('boom goes the dynamite!')
  })
```
JavaScript code can be added to the page in several ways.
1. Referenced with a `script` tag and `src` attribute.
  ```html
  <script src='example.js'></script>
  ```
1. Embedded within a `<script>` tag.
```html
<script>
const name = window.prompt('What is your name?', 'anonymous coward')
window.alert(`Hello ${name}, welcome to this web page.`)
</script>
```
1. Inline with specific `on`-event attributes on some HTML tags.
```html
<button onsubmit='window.alert(Math.random())'>Surprise me</button>
```

## APIs
Many web services publish data in JSON format. This format supports text, booleans, and numbers. It is structured into lists and key-value pairs.
```json
{
  "drink": "Kopi",
  "price": 1.20,
  "ingredients": [
    "water",
    "coffee",
    "condensed_milk"
  ],
  "sugar": true
}
```
Web pages can use JavaScript to retrieve request information from APIs.
```js
window.fetch('https://webuild.sg/api/v1/events')
  .then(response => response.json())
  .then(({ events }) => events.forEach(({ name, formatted_time}) => {
    document.body.innerText += `${name} at ${formatted_time}`
  }))
```

## Node.js
Web services are programmed in JavaScript using the Node.js environment, aka io.js.
- [io.js](https://iojs.org/)

This comes with NPM, the Node Package Manager, to offer access to a vast amount of free and open source code.
- NPM vs other developer ecosystems http://www.modulecounts.com/
- NPM community stats http://visual.ly/growth-npm

## Resources to help you along the way (including some GA classes)
