# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨




index.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>JavaScript DOM Manipulation</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1 id="main-title">Welcome to My Page</h1>
  </header>

  <main>
    <section>
      <p id="info-text">Click the button below to change this text and style!</p>
      <button onclick="changeTextAndStyle()">Change Text & Style</button>
    </section>

    <section>
      <p>Click the buttons to add or remove a paragraph:</p>
      <button onclick="addParagraph()">Add Paragraph</button>
      <button onclick="removeParagraph()">Remove Paragraph</button>
      <div id="dynamic-content"></div>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 My Website</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>





script.js

function changeTextAndStyle() {
  const text = document.getElementById("info-text");
  text.textContent = "The text has been changed dynamically!";
  text.style.color = "green";
  text.style.fontWeight = "bold";
  text.style.fontSize = "1.2rem";
}

function addParagraph() {
  const div = document.getElementById("dynamic-content");
  const newPara = document.createElement("p");
  newPara.textContent = "This is a new paragraph added to the DOM.";
  newPara.className = "added-paragraph";
  div.appendChild(newPara);
}

function removeParagraph() {
  const div = document.getElementById("dynamic-content");
  const lastPara = div.lastElementChild;
  if (lastPara) {
    div.removeChild(lastPara);
  }
}



style.css

body {
  font-family: Arial, sans-serif;
  padding: 20px;
}

button {
  margin: 5px;
  padding: 10px;
  cursor: pointer;
}

#dynamic-content {
  margin-top: 15px;
}

.added-paragraph {
  color: blue;
  font-style: italic;
}

