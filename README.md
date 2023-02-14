<h1 align="center"><img src="/img/vwc.gif" alt="Vets Who Code" width="100px" /> VETS WHO CODE</h1>

---

## [Prework](https://vetswhocode.io)

Welcome to the official Vets Who Code Prework! Here you'll find the tools, work, and accounts to prepare you for Vets Who Code's coursework.  We recommend you complete each section as they build upon one another. The prework should take a total of eight hours to complete.


 ### Accounts

Here are the accounts you will need to store your projects, solve problems, prototype, network, write, and be inspired by others' work. You'll also be able to see some fantastic projects from others.


#### [LinkedIn For Veterans](https://socialimpact.linkedin.com/programs/veterans/premiumform)

As a member of the U.S. military community, you can receive one year of LinkedIn Premium through SheerID's collaboration with LinkedIn. This service offers unlimited access to more than 10,000 courses through our LinkedIn Learning platform as a part of the program.

LinkedIn Learning is also pleased to offer eligible military spouses one year of access to LinkedIn Premium. As part of the program, you'll also gain access to more than 17,000 courses through LinkedIn Learning to help you manage your career and nurture your professional development.

LinkedIn Premium is a subscription-based service that offers users additional features not available on the free LinkedIn platform. These features include seeing who has viewed your profile, sending unlimited InMails to recruiters, and accessing exclusive content and events.

LinkedIn is a great way to connect with people with similar professional interests and network with potential hiring partners. We also have a LinkedIn Group that we would love for you to join!


#### [GitHub](https://github.com/)

GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

You can use GitHub to build software alongside millions of other developers. You can also use it to learn how to code, or find help with programming problems.

GitHub offers an easy way to share your code with friends and classmates, or collaborate on open-source projects.


#### [Dev.to](https://dev.to/)

If you're a developer looking for a career change or an aspiring developer who wants to learn more, Dev.to is the place to start.

Dev.to is an online community where developers from all backgrounds can share their experiences and expertise. It's also the perfect place for anyone interested in learning about software development to connect with like-minded individuals working in the field.

You can find jobs on Dev.to, as well as connect with recruiters and companies seeking employees with your skillset. You can also learn about new technologies, get advice on making the most of your experience and career path, and share tips on success in this industry.

Whether you're looking for a new job or want to meet other developers, Dev.to is an essential part of any aspiring developer's toolkit!
 
At #VetsWhoCode We Believe that long-form writing is one of the best ways to scale yourself, so you don't have to retain information, showcase how you communicate, and a simple way to advocate for yourself to non-technical employers when you're not writing since everyone on here is in tech so the people will be your audience.

### Command Line

The command line is a text-based interface for interacting with your computer. It's where you can type in commands to perform tasks like copying files, managing folders, and running applications.
 
It's often called the "command prompt" or "terminal," but it's also known as the "console" or "CLI," which stands for "command line interface." The application name used to access the command line differs from OS to OS: On Windows, it's called cmd (for Command Prompt), while on Mac, it's called Terminal.

Following will be the directions to operate in the command line for MacOS and Windows.

### Command Line Operations 

#### Open
You can use the Terminal app to access your computer's command line. The Terminal is one of the most powerful tools on your Mac, and it's how we'll be running our code.

MacOS: To open Terminal, go to Applications, then to Utilities finally to Terminal.
Windows: To open the command prompt, click Start and then click All Programs. In the programs list, click Accessories. In the accessories list, click Command Prompt.

#### Print Working Directory 

To help you know where you are currently in the Terminal we need to print the wordking directory. A directory would look like a folder on the screen of the GUI( Graphical User Interface). Type this command and hit enter:

MacOS: `pwd`
Windows: `cd`

#### List Directories
To list all the directories and files in your current location type:
MacOS : `ls`
Windows: `dir`

#### Make Directory

We want a place where we can put all our work in. While in the terminal make a new directory called VetsWhoCode by typing mkdir in Windows or MacOS and press enter:

`mkdir VetsWhoCode`

#### Change Working Directory

Now that we have made a new directory lets go there where we will put our work on our machine. te do that by in both windows and MacOS we do this by dyping cd then pressing enter:

`cd VetsWhoCode`


#### Change to previous Directory
If you want to go back to the previous directory for both Windows and MacOS you type this and press enter:

`cd ..`

#### Delete a directory
Let's say you make a typo and need to delete a directory. Here are the commands to do that.

MacOS; `rm -r NameOfDirectory`
Windows: `rmdir /S NameOfDirectory`

### Code Editor

An Integrated Development Environment (IDE) is a software application that provides comprehensive tools and features to assist developers in writing, debugging, and deploying software. An IDE typically includes a code editor, a debugger, a compiler or interpreter, and other tools such as a profiler, a version control system, and a build automation tool.
An IDE can also provide features like auto-completion, syntax highlighting, and code refactoring to make coding faster and more efficient. IDEs are commonly used for developing software applications, web applications, and mobile apps. Our preferred IDE is Visual Studio Code. Download it [here](https://code.visualstudio.com/). You can also install our developer extension pack by going to extensions and typing [VetsWhoCode Extension Pack](https://marketplace.visualstudio.com/items?itemName=VetsWhoCode.vetswhocode-extension-pack).

### Browser

The preferred browser for Vets Who Code is Google Chrome, due to its popularity and its robust developer tools. To download it please go [here](https://www.google.com/chrome/) and follow the prompts.


### Using GitHub
 We use GitHub extensively here. Below you’ll find the steps to use it within the terminal or command prompt.

1.	 Install Git: Git is a version control system used by GitHub. You can download and install Git for Windows from the official Git website.
2.	 Configure Git: After installing Git, open the Git Bash application and configure your name and email address using the following commands:
```console
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```



3.	Create a repository: A repository is a place where you can store and manage your code. Click on the “New” button and create a new repository.
![image](https://user-images.githubusercontent.com/24581531/218554688-7d3594a4-eb28-41f2-8683-8426d2783480.png)

4.	Clone the repository: To start working with the repository, you need to clone it to your local machine. You can do this by clicking on the “Code” button and copying the repository URL. Then, open your terminal or command prompt and type `git clone URL-Goes-Here`.
5.	Start coding: Once you have cloned the repository, you can change the code using your favorite code editor. To do this, open up the repository you just downloaded with VS Code (it's just a folder). Make text changes in files, create/remove folders and update their names. You're now coding.
6.	Stage your changes: You need to let `git` know what changes you made. To add your changes to the staging area, type `git add` followed by the file name or directory you want to add. You can use `git add .` to add all the changes. To make check what changes are staged you can run `git status`. In the output the file names in green are the changes that have been staged.
![image](https://user-images.githubusercontent.com/24581531/218550920-6430e103-d36d-472a-b6a2-c8445d72b338.png)
7.	Commit changes: Once you have added your changes to the staging area, you can commit them by typing `git commit -m "<commit message>"` followed by a brief description of the changes you made.
8.	Push changes: To upload your changes to the GitHub repository, type `git push`. If you're branch isn't setup check the output in the command line it may have a message like `git push --set-upstream origin <branch name>`. Once you've setup your upstream, you can use `git push` for all future uploads to this branch.
9.	Pull changes: If you've made changes on another computer to update your local machine run `git pull`.
10.	Create a pull request: If you want to suggest changes to someone else’s repository, you can create a pull request by clicking on the “Pull request” button on their repository page.
11.	Merge changes: The repository owner can merge your changes into their repository by clicking on the “Merge pull request” button.

### HTML && CSS
Hypertext Markup Language (HTML) is the standard language used to create web pages, while Cascading Style Sheets (CSS) is used to style and layout the content. Together, they form the building blocks of most websites.

1. Set up your environment: To create an HTML and CSS document, you'll need a text editor and a web browser. You can use any text editor, such as Notepad, Sublime Text, or Atom. You can also use online editors like CodePen or JSFiddle to get started quickly.

2. Create an HTML document: Open your text editor and create a new file. Save it with a .html extension. In this file, you will create the structure of your web page using HTML tags. Here's an example of a basic HTML document:

```
<!DOCTYPE html>
<html>
<head>
	<title>My First Web Page</title>
</head>
<body>
	<h1>Welcome to my website!</h1>
	<p>This is my first web page.</p>
</body>
</html>
```

3. Add content to the HTML document: Inside the body tags, you can add different types of content, such as headings, paragraphs, images, links, and lists. Here are a few examples:

```
<h1>This is a heading</h1>
<p>This is a paragraph.</p>
<img src="image.jpg" alt="An image">
<a href="https://www.example.com">Visit Example</a>
<ul>
	<li>Item 1</li>
	<li>Item 2</li>
	<li>Item 3</li>
</ul>
```

4. Create a CSS file: Create a new file in your text editor and save it with a .css extension. In this file, you will define the styles for your HTML document using CSS rules. Here's an example of a basic CSS rule:
```
h1 {
  color: red;
}
```

This rule sets the color of all h1 elements to red.

5. Link the CSS file to the HTML document: In the head section of your HTML document, add a link to your CSS file using the following code:

`<link rel="stylesheet" type="text/css" href="styles.css">`
This tells the browser where to find the CSS file that styles the HTML document.

6. Style the HTML document: Using CSS, you can change the font, color, background, and layout of your web page. Here are a few examples:
```
body {
  font-family: Arial, sans-serif;
  background-color: #f2f2f2;
}

h1 {
  color: #333;
  font-size: 36px;
}

p {
  color: #666;
  font-size: 18px;
}
```

These rules change the font family, background color, font size, and text color of different elements on the page.

### Javascript

JavaScript is a programming language used to create interactive and dynamic web pages. It's often used for client-side scripting, meaning it runs on the user's web browser.

Set up your environment: To start coding in JavaScript, you'll need a text editor and a web browser. 

1. Create an HTML document: Open your text editor and create a new file. Save it with a .html extension. In this file, you will create the structure of your web page using HTML tags. Here's an example of a basic HTML document:

```
<!DOCTYPE html>
<html>
<head>
	<title>My First JavaScript Program</title>
</head>
<body>
	<button onclick="myFunction()">Click me</button>
	<p id="demo"></p>
	<script>
		function myFunction() {
			document.getElementById("demo").innerHTML = "Hello, World!";
		}
	</script>
</body>
</html>
```

2. Add JavaScript to the HTML document: Inside the script tags, you can write JavaScript code. In this example, the code defines a function that changes the text of a paragraph element when a button is clicked.

Learn the basics of JavaScript syntax: JavaScript is a programming language, so it has its own syntax and rules. Here are a few basic concepts you should learn:

- **Variables**: You can declare variables using the `var`, `let`, or `const` keywords. Variables hold values that can be used later in your code. While var and let can have interchangable values, the value in `const` is not interchangeblae. Examples of how they:

```
var name = "John";
let age = 25;
const pi = 3.14;
```

- **Functions**: Functions are blocks of code that can be called later in your program. You can define functions using the function keyword, followed by the function name and any parameters. some examples:
```
function sayHello(name) {
  console.log("Hello, " + name + "!");
}
sayHello("Jody")

function square(number) {
  return number * number;
}

square(7)
```

- **Conditionals**: Conditionals are used to make decisions in your code based on certain conditions. You can use if, else if, and else statements to control the flow of your program. For example:

```
let grade = 85;

if (grade >= 90) {
  console.log("You got an A!");
} else if (grade >= 80) {
  console.log("You got a B!");
} else {
  console.log("You got a C or lower.");
}
```
- **Loops**: Loops are used to repeat a block of code a certain number of times. You can use for and while loops to iterate over arrays or perform other actions. For example:

```
let numbers = [1, 2, 3, 4, 5];

for (let i = 0; i < numbers.length; i++) {
  console.log(numbers[i]);
}

let count = 0;
while (count < 10) {
  console.log(count);
  count++;
}
```
- **Basic math operations**:
JavaScript supports basic math operations such as addition, subtraction, multiplication, and division. Here are a few examples:

```
let x = 5;
let y = 10;
let sum = x + y; // 15
let difference = y - x; // 5
let product = x * y; // 50
let quotient = y / x; // 2
```
- **Strings**:
Strings are used to represent text in JavaScript. You can declare strings using single or double quotes. Here are a few examples:
```
let greeting = "Hello, world!";
let name = 'John';
```

- **Arrays**:
Arrays are used to store a collection of data. You can create arrays using square brackets and separate the values with commas. Here are a few examples:
```
let numbers = [1, 2, 3, 4, 5];
console.log(numbers[2] // The answer will be 3 because in programming counting begins at zero

let colors = ["red", "green", "blue"];
console.log(colors[1]) // The answer will be green
```

- **String/Array methods** : JavaScript provides a number of built-in methods for working with strings and arrays. Here are a few examples:

```
// String methods
let message = "Hello, world!";
console.log(message.length); // 13
console.log(message.toUpperCase()); // "HELLO, WORLD!"
console.log(message.indexOf("world")); // 7

// Array methods
let numbers = [1, 2, 3, 4, 5];
console.log(numbers.length); // 5
console.log(numbers.reverse()); // [5, 4, 3, 2, 1]
console.log(numbers.join(", ")); // "5, 4, 3, 2, 1"
```
- **Objects (properties/methods)**:objects are key-value pairs used to represent real-world entities or concepts, as well as to organize and structure data.Here is an example:

```
// Create the object
const person = {
  name: 'Jody',
  age: 30,
  gender: 'male',
  sayHello: function() {
    console.log('Hello!');
  }
};

// Accessing the object

console.log(person.name); // Output: Jody
console.log(person['age']); // Output: 30
person.sayHello(); // Output: Hello!

// Adding or Updating the object
person.age = 35;
person.job = 'developer';
console.log(person.age); // Output: 35
console.log(person.job); // Output: developer

// Removing properties
delete person.gender;
console.log(person.gender); // Output: undefined
```

Use external JavaScript files: You can also create separate JavaScript files and link them to your HTML document using the `script` tag. This can help keep your code organized and easier to manage.

### Resources

If you want to learn a little bit more about these things or just want to be more prepared, these are our highly recommended resources.
- [Front End Masters Handbook](https://frontendmasters.com/guides/front-end-handbook/2019/)
- [Mozilla MDN](https://developer.mozilla.org/en-US/)
- [The Modern Javascript Tutorial](https://javascript.info/)
- [Getting To know HTML](https://learn.shayhowe.com/html-css/getting-to-know-html/)

### Capstone options

#### Operable Code
Upload your code to one of these services and have it run. You'll get a shareable URL that you can use to reference this code.
- [repl.it](https://replit.com/)
- [codepen](https://codepen.io/)
- [Github codespaces](https://github.com/features/codespaces)

#### Code Repository
You can use a code repository if you choose. However, please have a detailed README.md document explaining how the code runs and maybe screenshots of what it looks like when it runs.

