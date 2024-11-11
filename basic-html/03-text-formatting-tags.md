

## 🌟 Introduction
HTML text formatting tags are used to define and style the text content within an HTML document. These tags help in emphasizing, highlighting, and structuring the text, making it more readable and engaging. Below are detailed explanations of various text formatting tags along with examples.

### 💪 Bold and Importance

- **`<b>`: Bold Text**  
  **Description**: The `<b>` tag makes the enclosed text bold without adding any extra importance. This tag is purely for visual presentation and does not convey any special meaning to assistive technologies.  
  **Example**:
  ```html
  <b>This text is bold.</b>
  ```
  **Rendered**: **This text is bold.**

- **`<strong>`: Strong Importance**  
  **Description**: The `<strong>` tag indicates that the enclosed text is of strong importance or urgent. It not only makes the text bold but also conveys importance to assistive technologies like screen readers.  
  **Example**:
  ```html
  <strong>This text is strongly important.</strong>
  ```
  **Rendered**: **This text is strongly important.**

### ✨ Italics and Emphasis

- **`<i>`: Italic Text**  
  **Description**: The `<i>` tag italicizes the enclosed text without conveying any special emphasis or importance. It is used for stylistic purposes.  
  **Example**:
  ```html
  <i>This text is italic.</i>
  ```
  **Rendered**: *This text is italic.*

- **`<em>`: Emphasized Text**  
  **Description**: The `<em>` tag emphasizes the enclosed text, typically displaying it in italics. It conveys emphasis and stress to the text and can be nested for stronger emphasis.  
  **Example**:
  ```html
  <em>This text is emphasized.</em>
  ```
  **Rendered**: *This text is emphasized.*

### 📝 Underline and Small Text

- **`<u>`: Underlined Text**  
  **Description**: The `<u>` tag underlines the enclosed text. In modern HTML, it is used less frequently for stylistic purposes and more for denoting proper names or other terms that require underlining.  
  **Example**:
  ```html
  <u>This text is underlined.</u>
  ```
  **Rendered**: <u>This text is underlined.</u>

- **`<small>`: Smaller Text**  
  **Description**: The `<small>` tag renders the enclosed text in a smaller font size, typically for fine print, disclaimers, or other annotations.  
  **Example**:
  ```html
  <small>This text is smaller.</small>
  ```
  **Rendered**: <small>This text is smaller.</small>

### 🔶 Highlight and Deletion

- **`<mark>`: Highlighted Text**  
  **Description**: The `<mark>` tag highlights the enclosed text with a yellow background, indicating that the text is relevant or noteworthy.  
  **Example**:
  ```html
  <mark>This text is highlighted.</mark>
  ```
  **Rendered**: <mark>This text is highlighted.</mark>

- **`<del>`: Deleted Text**  
  **Description**: The `<del>` tag displays text that has been deleted or is no longer accurate, usually with a strikethrough.  
  **Example**:
  ```html
  <del>This text is deleted.</del>
  ```
  **Rendered**: <del>This text is deleted.</del>

### 📉 Subscript and Superscript

- **`<sub>`: Subscript Text**  
  **Description**: The `<sub>` tag renders the enclosed text as subscript, which is smaller and positioned below the baseline. It is often used for chemical formulas, mathematical expressions, and footnotes.  
  **Example**:
  ```html
  H<sub>2</sub>O is the chemical formula for water.
  ```
  **Rendered**: H<sub>2</sub>O is the chemical formula for water.

- **`<sup>`: Superscript Text**  
  **Description**: The `<sup>` tag renders the enclosed text as superscript, which is smaller and positioned above the baseline. It is often used for exponents, footnotes, and ordinal indicators.  
  **Example**:
  ```html
  E = mc<sup>2</sup> is Einstein's equation.
  ```
  **Rendered**: E = mc<sup>2</sup> is Einstein's equation.

### 💻 Code and Preformatted Text

- **`<code>`: Inline Code**  
  **Description**: The `<code>` tag displays a short fragment of computer code in a monospace font. It is used for inline code snippets and does not preserve whitespace or line breaks.  
  **Example**:
  ```html
  <code>console.log('Hello, world!');</code>
  ```
  **Rendered**: `<code>console.log('Hello, world!');</code>`

- **`<pre>`: Preformatted Text**  
  **Description**: The `<pre>` tag displays preformatted text in a fixed-width font, preserving whitespace, line breaks, and indentation. It is useful for code blocks, ASCII art, and other text that requires exact formatting.  
  **Example**:
  ```html
  <pre>
  function helloWorld() {
      console.log('Hello, world!');
  }
  </pre>
  ```
  **Rendered**:
  <pre>
  function helloWorld() {
      console.log('Hello, world!');
  }
  </pre>

### ⌨️ Keyboard Input and Sample Output

- **`<kbd>`: Keyboard Input**  
  **Description**: The `<kbd>` tag indicates text that represents user input from a keyboard, voice input, or any other text input device. It typically displays in a monospace font.  
  **Example**:
  ```html
  <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy.
  ```
  **Rendered**: <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy.

- **`<samp>`: Sample Output**  
  **Description**: The `<samp>` tag represents sample output from a computer program. It is typically displayed in a monospace font and is used to indicate text that the user sees as output.  
  **Example**:
  ```html
  <samp>Error: File not found.</samp>
  ```
  **Rendered**: <samp>Error: File not found.</samp>

### 🧮 Variables

- **`<var>`: Variable**  
  **Description**: The `<var>` tag indicates a variable in a mathematical expression or programming context. It is typically displayed in italics.  
  **Example**:
  ```html
  <var>x</var> = <var>y</var> + 2
  ```
  **Rendered**: <var>x</var> = <var>y</var> + 2

---
