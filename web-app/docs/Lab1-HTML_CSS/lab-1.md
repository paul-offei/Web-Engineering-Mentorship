# HTML Fundamentals (Heading Tags to Anchor Tags)

## 1. Introduction

HTML (HyperText Markup Language) is the standard markup language used to create and structure content on web pages. It provides elements for displaying text, creating lists, organizing information into tables, displaying images, collecting user input through forms, and navigating between web pages.

In this laboratory exercise, you will learn how to use important HTML elements to develop a simple Student Profile Web Page.

You will write HTML code, open the document in a web browser, and observe how the browser interprets and displays the HTML elements.

## 2. Learning Objectives

At the end of this laboratory exercise, students should be able to:

1. Create a basic HTML document.
2. Use heading tags to organize web page content.
3. Format text using paragraph tags.
4. Create ordered and unordered lists.
5. Organize information using HTML tables.
6. Display images using the HTML image element.
7. Create forms using different HTML form elements.
8. Navigate between web pages using hyperlinks.

## 3. Laboratory Setup

### 3.1 Required Software

You will need:

- A computer.
- A web browser (Google Chrome, Firefox, Microsoft Edge, etc.).
- A text editor or IDE (Visual Studio Code is recommended).

### 3.2 Creating Your First HTML Project

**Step 1:** Create a folder named `html-lab`.

**Step 2:** Open the folder in Visual Studio Code.

**Step 3:** Inside the folder, create a new file named `index.html`.

**Step 4:** Copy the following HTML code into the file.

**index.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Laboratory</title>
</head>
<body>

    <h1>HTML Hands-on Laboratory</h1>

</body>
</html>
```

**Step 5:** Save the file.

**Step 6:** Open the `index.html` file in your web browser. You can right-click the file and select Open with Browser.

You should see the heading:

HTML Hands-on Laboratory

**Note:** All the exercises in this laboratory will be added inside the `<body>` element of the `index.html` document.

---

# 2. HTML PRACTICAL EXERCISES

## 2.1 Heading Tags

HTML heading tags are used to introduce titles and subtitles on web pages. They help organize content into sections and subsections.

HTML provides six heading elements:

- `<h1>` – Largest heading.
- `<h2>` – Second-level heading.
- `<h3>` – Third-level heading.
- `<h4>` – Fourth-level heading.
- `<h5>` – Fifth-level heading.
- `<h6>` – Smallest heading.

### Practical Exercise

**Step 1:** Open your `index.html` file.

**Step 2:** Add the following code inside the `<body>` element, below your existing heading.

```html
<h1>Student Profile</h1>

<h2>Personal Information</h2>

<h3>Academic Information</h3>

<h4>Department of Computer Science</h4>

<h5>Web-Based Application Development</h5>

<h6>HTML Laboratory Exercise</h6>
```

**Step 3:** Save the file and refresh your browser.

**Observe:** Notice how the browser displays the headings in different font sizes. The `<h1>` element produces the largest heading, while `<h6>` produces the smallest.

### Your Task

Create a heading structure for a university website using all six heading elements.

Use the following topics:

- University Name
- Faculties
- School of Computing
- Department of Information Technology
- Programme of Study
- Course Title

---

## 2.2 Paragraph Tags

The paragraph element `<p>` is used to organize text into separate paragraphs.

Browsers generally ignore extra spaces, tabs, and line breaks in HTML source code. Therefore, simply pressing Enter several times in your HTML file does not create separate paragraphs on the web page.

To create separate paragraphs, wrap each paragraph with the `<p>` and `</p>` tags.

### Practical Exercise

**Step 1:** Add the following code below your heading tags.

```html
<h2>About Me</h2>

<p>
    My name is John Mensah. I am a student of the
    Department of Information Technology.
</p>

<p>
    I am interested in web development, database
    management, artificial intelligence, and software engineering.
</p>

<p>
    My goal is to become a professional web developer
    and build useful applications that solve real-world problems.
</p>
```

**Step 2:** Save your file and refresh the browser.

**Observe:** Each paragraph is displayed separately with vertical spacing between them.

### Your Task

Create an **About My University** section containing three paragraphs.

Your paragraphs should describe:

1. The name and location of your university.
2. The programmes offered by your university.
3. Why you chose to study your current programme.

---

## 2.3 List Tags

HTML lists are used to display related items in an organized format.

There are two major types of lists:

1. Ordered Lists.
2. Unordered Lists.

### 2.3.1 Ordered List Tags

An ordered list is used when items need to appear in a particular sequence. The browser automatically numbers the list items.

The following elements are used:

- `<ol>` – Defines an ordered list.
- `<li>` – Defines an individual list item.

### Practical Exercise

**Step 1:** Add the following code to your `index.html` file.

```html
<h2>Steps to Develop a Website</h2>

<ol>
    <li>Identify the purpose of the website.</li>
    <li>Plan the website structure.</li>
    <li>Create the HTML document.</li>
    <li>Add content to the web page.</li>
    <li>Test the website in a browser.</li>
</ol>
```

**Step 2:** Save the file and refresh your browser.

**Observe:** The browser automatically numbers the items from 1 to 5.

### 2.3.2 Unordered List Tags

An unordered list displays items using bullet points instead of numbers.

The following elements are used:

- `<ul>` – Defines an unordered list.
- `<li>` – Defines an individual list item.

### Practical Exercise

**Step 1:** Add the following code below the ordered list.

```html
<h2>Programming Languages</h2>

<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
    <li>Python</li>
    <li>Java</li>
</ul>
```

**Step 2:** Save the file and refresh your browser.

**Observe:** The browser displays the programming languages using bullet points.

### Your Task

Create two lists for your university profile:

**List 1: My Favourite Courses**

Use an ordered list to display five courses you are interested in.

**List 2: My Hobbies**

Use an unordered list to display at least five hobbies.

---

## 2.4 Table Tags

HTML tables are used to organize information into rows and columns.

Tables are useful when displaying structured information such as student records, examination results, employee information, and product details.

The following HTML elements are commonly used:

| HTML Element | Description |
|---|---|
| `<table>` | Defines a table. |
| `<tr>` | Defines a table row. |
| `<th>` | Defines a table heading cell. |
| `<td>` | Defines a table data cell. |
| `<thead>` | Groups the table heading section. |
| `<tbody>` | Groups the main table content. |
| `<tfoot>` | Groups the table footer. |

### Practical Exercise

Assume you want to display the academic records of students in a table.

**Step 1:** Add the following code to your `index.html` file.

```html
<h2>Student Academic Records</h2>

<table border="1" width="100%">

    <thead>
        <tr>
            <th>Student ID</th>
            <th>Student Name</th>
            <th>Programme</th>
            <th>Level</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>IT001</td>
            <td>John Mensah</td>
            <td>Information Technology</td>
            <td>200</td>
        </tr>

        <tr>
            <td>IT002</td>
            <td>Mary Owusu</td>
            <td>Computer Science</td>
            <td>300</td>
        </tr>

        <tr>
            <td>IT003</td>
            <td>Peter Asare</td>
            <td>Information Technology</td>
            <td>400</td>
        </tr>
    </tbody>

</table>
```

**Step 2:** Save the file and refresh your browser.

**Observe:** The browser displays the student records in rows and columns.

### Understanding the Code

1. The `<table>` element creates the table.
2. The `<thead>` element groups the column headings.
3. The `<tr>` element creates a new row.
4. The `<th>` element creates a heading cell.
5. The `<tbody>` element contains the student records.
6. The `<td>` element creates individual data cells.

### Your Task

Create a table titled **My Course Registration** with the following columns:

- Course Code
- Course Title
- Credit Hours
- Lecturer

Include at least five courses in your table.

---

## 2.5 Image Tags

Images make web pages more attractive and help communicate information visually.

HTML uses the `<img>` element to display images.

The most important attributes include:

| Attribute | Description |
|---|---|
| `src` | Specifies the location of the image. |
| `alt` | Provides alternative text describing the image. |
| `width` | Specifies the image width. |
| `height` | Specifies the image height. |

The `<img>` element does not require a closing tag.

### Practical Exercise

**Step 1:** Create a folder named `images` inside your `html-lab` folder.

Your project should now look like this:

```text
html-lab/
│
├── index.html
│
└── images/
```

**Step 2:** Download or copy a picture of a computer, laptop, or student and save it inside the `images` folder.

Name the image `computer.jpg` (retain the actual file extension).

Your project should now look like this:

```text
html-lab/
│
├── index.html
│
└── images/
    └── computer.jpg
```

**Step 3:** Add the following code inside your HTML document.

```html
<h2>My Favourite Technology</h2>

<p>Below is an image of a computer:</p>

<img src="images/computer.jpg"
     alt="A computer"
     width="400">
```

**Step 4:** Save your file and refresh the browser.

**Observe:** The browser displays the computer image.

### Loading an Image from the Internet

Images can also be displayed using an image URL.

Add the following code below your previous image.

```html
<h2>Online Image</h2>

<img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085"
     alt="Computer programming workspace"
     width="400">
```

**Observe:** The browser attempts to load the image directly from the internet.

**Note:** An internet connection is required for remotely hosted images. Always provide meaningful alternative text using the `alt` attribute.

### Your Task

Create a section titled **My University**.

1. Find an image of your university or campus.
2. Save the image inside your `images` folder.
3. Display the image using the `<img>` element.
4. Set its width to 500 pixels.
5. Provide an appropriate alternative text.

---

## 2.6 Form Tags

HTML forms are used to collect information from users.

Forms are important in web applications because they allow users to enter information such as names, email addresses, passwords, dates, and other details.

Common HTML form elements include:

| HTML Element | Purpose |
|---|---|
| `<form>` | Defines a form. |
| `<label>` | Provides a description for a form field. |
| `<input>` | Creates different types of input fields. |
| `<textarea>` | Allows users to enter long text. |
| `<select>` | Creates a dropdown list. |
| `<option>` | Defines an option in a dropdown list. |
| `<button>` | Creates a clickable button. |

### 2.6.1 Text Input Fields

Text input fields allow users to enter a single line of text.

The `<input>` element uses the `type` attribute to specify the kind of information the user should enter.

Some commonly used input types are:

- `text`
- `password`
- `email`
- `number`
- `date`
- `range`

### Practical Exercise

**Step 1:** Add the following code to your HTML document.

```html
<h2>Student Registration Form</h2>

<form>

    <label for="student-name">Full Name:</label>
    <input type="text"
           id="student-name"
           placeholder="Enter your full name">

    <br><br>

    <label for="student-id">Student ID:</label>
    <input type="text"
           id="student-id"
           placeholder="Enter your student ID">

    <br><br>

    <label for="password">Password:</label>
    <input type="password"
           id="password"
           placeholder="Enter your password">

</form>
```

**Step 2:** Save your file and refresh the browser.

**Observe:** The browser displays three input fields.

The password field hides the characters entered by the user.

**Understanding the Code:**

- `type="text"` creates a text input field.
- `type="password"` creates a password field.
- `placeholder` displays a hint inside the input field.
- `id` uniquely identifies the input element.
- The label's `for` attribute associates the label with the corresponding input field.

### 2.6.2 Email, Number and Date Input Fields

HTML provides specialized input types for collecting different categories of information.

**Practical Exercise**

Add the following code inside your existing `<form>` element.

```html
<h3>Additional Information</h3>

<label for="email">Email Address:</label>
<input type="email"
       id="email"
       placeholder="example@gmail.com">

<br><br>

<label for="age">Age:</label>
<input type="number"
       id="age"
       min="16"
       max="60">

<br><br>

<label for="dob">Date of Birth:</label>
<input type="date"
       id="dob">

<br><br>

<label for="rating">Rate Your Computer Skills:</label>
<input type="range"
       id="rating"
       min="1"
       max="10"
       value="5">
```

**Observe:**

- The email field is designed for email addresses.
- The number field accepts numerical values.
- The date field provides a date selector.
- The range field provides a slider.

### 2.6.3 Textarea

The `<textarea>` element allows users to enter multiple lines of text.

It is useful for collecting information such as biographies, comments, descriptions, and feedback.

**Practical Exercise**

Add the following code inside your form.

```html
<h3>Student Biography</h3>

<label for="biography">About Yourself:</label>

<br>

<textarea id="biography"
          rows="5"
          cols="40"
          placeholder="Write something about yourself">
</textarea>
```

**Observe:** The browser displays a larger text input area where users can enter multiple lines of text.

### 2.6.4 Dropdown Lists

Dropdown lists allow users to select an option from a predefined list.

The `<select>` element defines the dropdown, while the `<option>` element defines each available choice.

**Practical Exercise**

Add the following code inside your form.

```html
<h3>Programme Selection</h3>

<label for="programme">Select Your Programme:</label>

<br>

<select id="programme">

    <option value="">-- Select Programme --</option>

    <option value="IT">Information Technology</option>

    <option value="CS">Computer Science</option>

    <option value="SE">Software Engineering</option>

    <option value="MIS">Management Information Systems</option>

</select>
```

**Observe:** The browser displays a dropdown list containing four academic programmes.

### 2.6.5 Radio Buttons

Radio buttons allow users to select only one option from a group of alternatives.

Radio buttons belonging to the same group should share the same `name` attribute.

**Practical Exercise**

Add the following code inside your form.

```html
<h3>Gender</h3>

<input type="radio"
       name="gender"
       id="male"
       value="Male">

<label for="male">Male</label>

<br>

<input type="radio"
       name="gender"
       id="female"
       value="Female">

<label for="female">Female</label>
```

**Observe:** The user can select either Male or Female, but not both.

### 2.6.6 Checkboxes

Checkboxes allow users to select one or more options from a group.

Unlike radio buttons, multiple checkboxes can be selected at the same time.

**Practical Exercise**

Add the following code inside your form.

```html
<h3>Areas of Interest</h3>

<input type="checkbox"
       id="web"
       name="interest"
       value="Web Development">

<label for="web">Web Development</label>

<br>

<input type="checkbox"
       id="database"
       name="interest"
       value="Database Management">

<label for="database">Database Management</label>

<br>

<input type="checkbox"
       id="ai"
       name="interest"
       value="Artificial Intelligence">

<label for="ai">Artificial Intelligence</label>

<br>

<input type="checkbox"
       id="cybersecurity"
       name="interest"
       value="Cybersecurity">

<label for="cybersecurity">Cybersecurity</label>
```

**Observe:** The user can select multiple areas of interest.

### 2.6.7 Buttons

The `<button>` element creates a clickable button on a web page.

Buttons are commonly used to submit forms or trigger actions.

**Practical Exercise**

Add the following code at the end of your registration form, before the closing `</form>` tag.

```html
<br><br>

<button type="submit">Register</button>

<button type="reset">Clear Form</button>
```

**Observe:**

- The Register button is designed to submit the form.
- The Clear Form button resets the form fields to their initial values.

**Note:** These buttons do not automatically store student information. Processing and storing submitted data require additional technologies, such as server-side programming and databases.

### Your Task

Create a complete **Student Registration Form** containing:

1. Full Name.
2. Student ID.
3. Password.
4. Email Address.
5. Age.
6. Date of Birth.
7. Biography.
8. Programme Selection (dropdown).
9. Gender (radio buttons).
10. Areas of Interest (checkboxes).
11. Register and Clear Form buttons.

Ensure that every input field has an appropriate label.

---

## 2.7 Anchor Tags

Anchor tags are used to create hyperlinks that allow users to navigate from one web page to another.

The `<a>` element is used to create hyperlinks.

The `href` attribute specifies the destination of the link.

Anchor tags can be used to:

1. Navigate to external websites.
2. Navigate to other pages within the same website.
3. Navigate to specific sections within a web page.

### 2.7.1 Linking to External Websites

External links direct users to websites hosted on other domains.

**Practical Exercise**

Add the following code to your `index.html` file.

```html
<h2>Useful Websites</h2>

<p>
    Visit
    <a href="https://www.google.com">
        Google
    </a>
    to search for information.
</p>

<p>
    Visit
    <a href="https://www.wikipedia.org">
        Wikipedia
    </a>
    to read educational articles.
</p>
```

**Step 2:** Save your file and refresh the browser.

**Observe:** The browser displays clickable links. Clicking a link takes you to the corresponding external website.

### 2.7.2 Linking to Another HTML Page

Anchor tags can also navigate between different HTML documents within the same website.

**Practical Exercise**

**Step 1:** Inside your `html-lab` folder, create another HTML file named `about.html`.

Your project should now look like this:

```text
html-lab/
│
├── index.html
│
├── about.html
│
└── images/
    └── computer.jpg
```

**Step 2:** Add the following code to `about.html`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>About Page</title>
</head>

<body>

    <h1>About My Website</h1>

    <p>
        Welcome to my student profile website.
        This page contains additional information about me.
    </p>

    <a href="index.html">Back to Home Page</a>

</body>
</html>
```

**Step 3:** Return to `index.html` and add the following code.

```html
<h2>Website Navigation</h2>

<a href="about.html">About Me</a>
```

**Step 4:** Save both files and open `index.html` in your browser.

**Step 5:** Click the About Me link.

**Observe:** The browser navigates from `index.html` to `about.html`.

Clicking the Back to Home Page link takes you back to `index.html`.

### 2.7.3 Linking to a Specific Section

An anchor can also take a user to a particular section within the same web page.

This is achieved using the `id` attribute.

**Practical Exercise**

Add the following code to your HTML document.

```html
<h2>Page Navigation</h2>

<a href="#contact">Go to Contact Section</a>

<br><br>

<h2 id="contact">Contact Information</h2>

<p>Email: student@example.com</p>

<p>Phone: 0200000000</p>
```

**Observe:** Clicking the Go to Contact Section link navigates to the section identified by `id="contact"`.

### Your Task

Create a simple website containing three HTML documents:

1. `index.html` – Home page.
2. `about.html` – About page.
3. `contact.html` – Contact page.

Add hyperlinks that allow users to navigate between all three pages.

Also include at least two external website links on your home page.

---

# 3. FINAL PRACTICAL EXERCISE

## Developing a Student Profile Website

Now that you have practised the important HTML elements, combine them to create a simple Student Profile Website.

Your website should contain the following sections:

### 3.1 Home Page

Create a home page containing:

- A main heading displaying your name.
- A short paragraph introducing yourself.
- Your photograph.
- A list of your interests.
- A hyperlink to your About page.
- A hyperlink to your Contact page.

### 3.2 About Page

Create an About page containing:

- A heading titled About Me.
- Three paragraphs describing yourself.
- An ordered list of your educational qualifications.
- An unordered list of your hobbies.
- A table showing your academic information.
- A hyperlink to return to the Home page.

### 3.3 Contact Page

Create a Contact page containing:

- Your contact information.
- Your email address.
- Your telephone number.
- A contact form containing:
  - Full Name.
  - Email Address.
  - Subject.
  - Message (textarea).
  - Submit button.
- A hyperlink to return to the Home page.

### Suggested Project Structure

Organize your project as follows:

```text
student-profile/
│
├── index.html
│
├── about.html
│
├── contact.html
│
└── images/
    └── profile.jpg
```

## 4. Laboratory Review

Before completing the laboratory, ensure that you can explain the following HTML elements.

| No. | HTML Element | What It Does |
|---|---|---|
| 1 | `<h1>` – `<h6>` | Creates headings. |
| 2 | `<p>` | Creates paragraphs. |
| 3 | `<ol>` | Creates ordered lists. |
| 4 | `<ul>` | Creates unordered lists. |
| 5 | `<li>` | Defines list items. |
| 6 | `<table>` | Creates tables. |
| 7 | `<tr>` | Creates table rows. |
| 8 | `<th>` | Creates table headings. |
| 9 | `<td>` | Creates table data cells. |
| 10 | `<img>` | Displays images. |
| 11 | `<form>` | Defines forms. |
| 12 | `<input>` | Creates input fields. |
| 13 | `<textarea>` | Creates multiline text fields. |
| 14 | `<select>` | Creates dropdown lists. |
| 15 | `<option>` | Defines dropdown options. |
| 16 | `<button>` | Creates buttons. |
| 17 | `<a>` | Creates hyperlinks. |

## 5. Submission Requirements

Submit your completed HTML project by `Publishing Your Website Using GitHub Pages` containing:

1. `index.html`
2. `about.html`
3. `contact.html`
4. An `images` folder containing your selected image.

Ensure that:

- All HTML files open successfully in a web browser.
- All images display correctly.
- Tables and lists are properly structured.
- Form elements display correctly.
- Internal hyperlinks navigate to the correct pages.
- External hyperlinks open the intended websites.
- Your HTML code is properly indented and organized.

**End of Laboratory Hands On Exercise**