# HTML Code

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <style>
      .box3 {
        background-color: lightgreen;
      }

      .box p {
        font-size: 20px;
      }

      .box > p {
        border: 2px solid blue;
      }

      .innerbox + div {
        background-color: lightcoral;
      }

      .innerbox ~ div {
        background-color: aqua;
      }

      label[for] {
        color: red;
      }

      /* for more specific */

      label[for="email"] {
        background-color: lightblue;
      }

      input[type] {
        background-color: lightseagreen;
      }

      a[href] {
        text-decoration: none;
      }
    </style>
    <h1>This is about page</h1>

    <div class="box">
      <div class="innerbox">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim nobis
          deserunt officiis harum dolore? Nisi incidunt quae, hic quia, mollitia
          odio molestiae aliquam reprehenderit qui quas dolor corporis fuga
          recusandae!
        </p>
        <p id="pargraph">this is second p tag;</p>
      </div>
      <div class="box2">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus
          est explicabo, consequuntur laboriosam unde, sit quos deserunt tempora
          eaque doloribus aperiam soluta cum voluptate neque veniam rerum velit!
          Eius, vero.
        </p>
      </div>
      <div class="box2">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus
          est explicabo, consequuntur laboriosam unde, sit quos deserunt tempora
          eaque doloribus aperiam soluta cum voluptate neque veniam rerum velit!
          Eius, vero.
        </p>
      </div>
      <p>this is another p tag in side box class</p>
    </div>

    <div class="box3">this is box 3 content</div>

    <form onsubmit="getFormValue($event)">
      <label for="email">Email: </label>
      <input type="text" name="email" />
      <label for="password">Password: </label>
      <input type="password" name="password" />
      <button type="submit">Submit</button>
    </form>

    <a href="#">LINK TO ANYTHING</a>

    <script>
      const getFormValue = ($event) => {
        console.log("this is form value: ", $event);
      };
    </script>
  </body>
</html>
```

# HTML Explanation

This document contains an HTML structure styled using embedded CSS and a basic form submission functionality with JavaScript.

## 1. HTML Structure

The basic structure of the HTML consists of:

- **Head Section**:
  - Includes meta tags for character encoding (`UTF-8`) and viewport settings for responsive design.
  - Contains the document title: "Document".
- **Body Section**:
  - Contains the styling and content.
  - Includes a heading (`<h1>`) and various `<div>` containers with paragraphs (`<p>` tags).
  - A form section with input fields for "Email" and "Password".
  - A link (`<a>`) with no destination (href set to `"#"`).

## 2. CSS Styles

### Classes and Selectors:

- `.box3`: Sets the background color to light green.
- `.box p`: Targets all `<p>` elements inside the `.box` class and increases the font size to 20px.
- `.box > p`: Targets direct child `<p>` elements of `.box` and adds a 2px solid blue border.
- `.innerbox + div`: Selects the immediate sibling `div` after `.innerbox` and sets its background to light coral.
- `.innerbox ~ div`: Selects all siblings of `.innerbox` after the first `div` and sets their background to aqua.

### Attribute Selectors:

- `label[for]`: Applies red text color to all `<label>` elements with a `for` attribute.
- `label[for="email"]`: Specifically targets the label with a `for="email"` attribute and gives it a light blue background.
- `input[type]`: Targets all `<input>` elements by their `type` attribute and changes their background to lightseagreen.
- `a[href]`: Removes the underline from links that contain an `href` attribute.

## 3. JavaScript

- **Form Submission**:
  - The `onsubmit` event of the form triggers the `getFormValue()` function, which logs the form submission event (`$event`) to the console.

## 4. Example Content

- **Main Heading**: "This is about page"
- **Text in `.box` class**: Contains two paragraphs and additional text, followed by `.box2` class content.
- **Form**: Input fields for email and password with a submit button.
