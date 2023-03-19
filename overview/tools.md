# 🛠 Tools

### IDE

Now that you know the basics of Web Development you are ready to go and write some code!

But there is still a question left to answer: Where do programmers write their code?

As we have already pointed out, you could start programming in the default text editor of your operating system, however take our word when we say: Don’t. You will regret it. Most developers use an Integrated Development Environment (IDE) to write code because it comes with a lot of handy features that help developers code faster and cleaner. Once you get used to an IDE, you will never look back. Let’s look at some reasons they’re so handy.

#### **1. Graphical User Interface**

The GUI of an IDE has been designed in a way that allows you to see your project directory, editor and terminal all at once. This makes it very easy to navigate between the different html, css and javascript files.

#### **2. Autocomplete**

If the IDE knows your programming language it can anticipate what you are going to type next and thus allow for faster development.

#### **3. Syntax Highlighting**

An IDE that knows the syntax of your programming language can provide visual cues. Keywords, words that have special meaning like if, for or while in JavaScript, are highlighted with different colors.

#### **4. Debugging**

No one can avoid to write code without errors. IDEs provide hints while coding to prevent errors before compilation and help you with debugging afterwards.

Some popular IDEs for Web Development are Visual Studio Code, Vim and Sublime Text 3. In the Udemy course your instructor will use Visual Studio Code. Feel free to check it out [here](https://code.visualstudio.com/).

For this course and your project, you will use the online code editor [CodeSandbox](https://codesandbox.io/). We will set up the environment together in the first Meetup. This IDE is based on the same platform as Visual Studio Code, but offers some additional functionalities. The user interface has been designed in a way that allows you to see your file directory, editor, and your executed program all at once. CodeSandbox allows you to create teams that can not only access the same files but also make it possible to have live coding session together. To sign up you only need a free Github account, which you can create in a matter of seconds.

### Udemy

For this course you will be working with the [The Web Development Bootcamp 2022](https://www.udemy.com/course/the-web-developer-bootcamp/) on Udemy.

This course is filled with a ton of content. For our project we are only focusing on the front-end so you can naturally ignore (for now) the later half of the course, which exclusively deals with the back-end. We encourage you to do all the exercises you will encounter in between. You are going to learn a lot by doing the exercises and programming on your project will become far simpler.

The following sections should leave you with enough knowledge to complete your project:

| Section Name                          | Duration (h) |
| ------------------------------------- | ------------ |
| Course Orientation                    | 0.5          |
| An Introduction to Web Development    | 0.75         |
| CSS: The Very Basics                  | 1            |
| CSS: The World of CSS Selectors       | 1.25         |
| The CSS Box Model                     | 1            |
| Responsive CSS & Flexbox              | 1.25         |
| JavaScript Basics!                    | 1            |
| JavaScript String and More            | 0.75         |
| JavaScript Decision Making            | 1.25         |
| JavaScript Arrays                     | 1            |
| JavaScript Object Literals            | 0.75         |
| JavaScript Repeating Stuff With Loops | 1.5          |
| NEW: Introducing Functions            | 0.5          |
| Leveling Up Our Functions             | 1            |
| Callbacks & Array Methods             | 1.5          |
| Introducing The World Of The DOM      | 1.75         |
| The Missing Piece: DOM Events         | 1.75         |

### API

For this semester project you will also need to learn about APIs. But what exactly is an API? An API (Application Programming Interface) allows different devices to connect to each other and send, update and request data from one to the other. You can think of it as a waiter in a restaurant. The waiter takes and understands your order, delivers it to the kitchen and comes back with the requested order. APIs function in a similar way.

#### How do we get the data?

Every API is unique but if you understand how to obtain output from one API you will know how to get data from all. For the most part, APIs are accessed through URLs, and the specifics of how to query these URLs change based on the specific service you are using. For example, the [TVMAZE API](https://www.tvmaze.com/api), that we will be using in our project, has several types of data that you can request. To search through all the shows in their database by the show’s name you can use the following URL.

```url
https://api.tvmaze.com/search/shows?q=girls
```

You can see that we access the URL and append our searchterm to it. The server will understand what we want and will return a response with all necessary information. To use some APIs you might need to create an account to obtain an API key. By doing this the server will know who requested an information and will block your account if you send too many API requests. To use the API for your project you don’t need an account.

Congrats, you have made your first API request!

So how do we actually get the data from an API into our code?

In JavaScript we use the [Fetch API](https://developer.mozilla.org/de/docs/Web/API/Fetch\_API) to make our API call. You will learn more about how to use it in section [28](https://www.udemy.com/course/the-web-developer-bootcamp/learn/lecture/22051352#overview) of the Udemy course which will also go over [JSON](https://tech-academy-ev.github.io/WiSe22\_Shows\_App\_Guide/additional-resources.html#json), the text format of the weather data.\
To provide you with a template for later on and as a reminder, this is one way of how to deal with fetch:

```javascript
async function exampleAPICall() {
  try {
    const response = await fetch(
      "https://api.tvmaze.com/search/shows?q=girls"
    );
    const data = await response.json();
    /* your code here to work with the data */
  } catch (error) {
    console.log(error);
  }
}
```
