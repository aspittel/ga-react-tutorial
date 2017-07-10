# Introduction to React

## Overview
In this workshop, we will be learning the basics of the React JavaScript framework and building a sample project using the technologies learned.
* React encourages reusable, maintainable, and interactive front-end code.

## Learning Objectives
* Understand what makes React different from other JavaScript frameworks and JavaScript without a framwork.
* Install and setup React.
* Understand best practices for React setup.
* Introduce concept of state in React.
* Introduce concept of interactivity in React.
* Work on building a sample status widget.

## Introduction to React
React is a web framework developed by Facebook in order to make elements of user interfaces more modular and easier to maintain. According to React's website it is used to "Build encapsulated components that manage their own state, then compose them to make complex UIs."

#### Example: Facebook Reactions
* Imagine you worked at Facebook when they wanted to shift from using likes to reactions.
* Look at your Facebook and see how many different places reactions are used.
* Using traditional JavaScript, HTML, and CSS would it be easy and to implement these reactions in multiple places? Would there be repeated code between the different reaction components?
* React makes it easy to utilize UI components in multiple locations because instead of separating your HTML and JavaScript code, it uses JavaScript in order to write your HTML code.

#### Exercise: TODO MVC
* With the other people at your table, look at the code on the [TodoMVC](http://todomvc.com/) website. This site shows the same to do list application written in a bunch of different front end frameworks. 
* For this exercise, look at the [VanillaJS](http://todomvc.com/examples/vanillajs/) and [React](http://todomvc.com/examples/react/#/) examples on their site.
* Vanilla is what developers use to refer to JavaScript that doesn't make use of a framework.
* If you know another front-end framework like Angular, VueJS, or JQuery, it may be helpful to look at their implementations after this workshop.
* On the side of the page, there are links to Github source code for each version of the code. Go ahead and look through the files and see what differences there are between the implementations. 
* At the end, each table will point out what differences they found between the React and VanillaJS versions of TODO MVC.

#### Alternate Exercise: IMDBExplorer
* Same as above but with my IMDBExplorer app from my GA Code Sample.
* Pro: Much simpler code, similar to how I was envisioning the code for this workshop to look.
* Cons: Would rather not use my code, maybe not perfect implementation.

## Installing React

#### Our Set Up vs. Production Set Up
For this workshop, due to time constraints, we will be using CDN versions of React, Babel (a compiler that allows us to use next generation JavaScript features), Bootstrap's CSS, and FontAwesome Icons. CDNs allow us to use resources hosted on other sites within our code. In a production environment, however, it is inefficient to ping another website to retrieve an asset. A production-ready React application would most likely use a bundler, most commonly Webpack, to combine the React.js code and any other JavaScript libraries we use with our own code. Using Webpack (and a development server) would also allow us to split up our React code into multiple files. I usually have each React class that I build in a separate file. A good resource that goes further in depth on Webpack is [here](http://blog.andrewray.me/webpack-when-to-use-and-why/).

#### Project Set Up
* For this workshop, the only technical tool you need installed is a text editor and a web browser. If you do not have one installed, please go ahead and download [Sublime Text](https://www.sublimetext.com/) or [Atom](https://atom.io/).
* If you have git installed on your computer, clone this repository. If not, you can also click the download button on the GitHub site to download the starter code files.
* Open the `START.html` file on your computer in both your text editor and in the browser. 
* Also open the `REACT.html` file in another tab in your text editor.
* This file has HTML and CSS code that we will be translating to React code. If you have extra time, feel free to play around with the styling and layout.

# Project: Recreating a Facebook Status Widget in React
## React Components
If you open up the REACT.html file included in the repository you downloaded from GitHub, you will see a Hello World React component written in the file to start out.
```javascript
        <div id="root"></div>
        <script type="text/jsx">
            // Uses a JavaScript class that extends the React Component class
            class HelloWorld extends React.Component {
                render () {
                    // Tells React what HTML code to render
                    return (
                        <div>
                            <h1>Hello World</h1>
                        </div>
                    )
                }
            }
                        
            // Tells React to attach the HelloWorld component to the 'root' HTML div
            ReactDOM.render(
                <HelloWorld />,
                document.getElementById('root')
            )
        </script>
```
Let's walk step by step through this code.

* The JavaScript code starts out with declaring a class called `HelloWorld` which is a subclass of the React.Component class, which we get from the React CDN we have included at the top of the HTML file. To read more about JavaScript classes, [this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes) is a great resource.

* Within the `HelloWorld` class, we declare a render method which returns the HTML code that we want our component to display. In this case, that is a simple "Hello World" message, but you will see later on that what we render can be much more complex and interactive.

* Finally, we tell React which component we want to render as well as which HTML element we want to attach that component to. 

#### Exercise: Renaming and Replacing Components
* Rename the component to `Status` and make the component render the HTML code from the `START.html` file.

## State
## Event listeners
## Conditional Properties 
## Props???
## We Do: Text Box and Likes for Facebook Post Widget

## You Do: Changing Likes to Reactions

## Next Steps
