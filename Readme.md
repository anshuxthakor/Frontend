# Frontend Learning Repository

A personal frontend development learning repository containing exercises, experiments, notes, and small projects built while learning modern web development.

This repository documents my progress from basic JavaScript and DOM manipulation to React, Redux Toolkit, TypeScript, API integration, routing, authentication, and feature-based application architecture.

> This is a learning repository, so some projects are experimental, incomplete, or intentionally written in different styles while exploring new concepts so check accordingly.

---

## About This Repository

The purpose of this repository is to store everything I build while learning frontend development.

Instead of keeping every project in one large application, the projects are organized into separate folders. Each folder focuses on a specific technology or concept.

The repository currently contains:

- JavaScript exercises
- DOM manipulation projects
- Local Storage examples
- React applications
- React Router examples
- Context API experiments
- Authentication flows
- Redux Toolkit applications
- API integration projects
- TypeScript fundamentals
- React with TypeScript
- Notes and learning diagrams

---

## Technologies Used

The repository mainly uses the following technologies:

- HTML
- CSS
- JavaScript
- TypeScript
- React
- Redux Toolkit
- React Router
- Vite
- Axios
- Local Storage
- ESLint
- TanStack-related experiments

---

## Repository Structure

```text
Frontend/
├── JavaScript/
├── ReactJs/
├── ReduxToolkit/
└── TypeScript/
```

Each top-level directory represents a different stage or area of frontend development.

---

# JavaScript

The `JavaScript` directory contains beginner and intermediate JavaScript exercises.

These projects focus on understanding the language itself before using frameworks such as React.

```text
JavaScript/
├── 01/
├── 02/
├── 03/
├── 04/
├── 05/
├── 06/
├── 07/
├── 08/
├── 09/
├── 10/
├── 11/
├── Dom/
├── LocalStorage/
└── Readme.md
```

## What JavaScript Projects Teach

The JavaScript exercises cover:

- Variables
- Data types
- Type conversion
- Conditions
- Loops
- Functions
- Callbacks
- Higher-order functions
- Arrays
- Objects
- Destructuring
- Spread and rest operators
- The `this` keyword
- Prototypes
- Classes
- DOM manipulation
- Event listeners
- Browser storage

---

## JavaScript Lessons

### JavaScript/01 — Basics and Data Types

This folder introduces the basic building blocks of JavaScript.

It includes examples of:

- Variables
- Arithmetic operations
- Primitive data types
- Non-primitive data types
- `Symbol`
- `NaN`
- Console methods such as:

```js
console.log();
console.warn();
console.error();
console.table();
```

This is a good starting point for understanding how JavaScript values work.

---

### JavaScript/02 — Type Conversion and Conditions

This project focuses on how JavaScript converts values from one type to another.

Topics include:

- Implicit type conversion
- Explicit type conversion
- Converting strings to numbers
- Converting values to booleans
- Using `prompt()`
- Conditional statements
- `if`, `else if`, and `else`
- Basic grading logic
- Introduction to `switch`

This lesson helps explain why expressions such as the following can behave differently:

```js
"5" + 2;
"5" - 2;
Boolean(0);
Number("10");
```

---

### JavaScript/03 — Loops and Strings

This folder explores repetition and string manipulation.

Topics include:

- `while` loops
- `do...while` loops
- `for` loops
- `let`, `const`, and `var`
- Template literals
- String methods

Examples of string methods covered include:

```js
.length
.split()
.slice()
.replace()
.repeat()
.trim()
.startsWith()
```

These concepts are important when working with user input and collections of data.

---

### JavaScript/04 — Functions and Callbacks

This project explains how functions work in JavaScript.

Topics include:

- Function declarations
- Function expressions
- Arrow functions
- Default parameters
- Immediately Invoked Function Expressions
- Pure functions
- Impure functions
- Return values
- Callbacks
- First-class functions
- Higher-order functions

A higher-order function is a function that either accepts another function as an argument or returns another function.

Example:

```js
const createMultiplier = (number) => {
  return (value) => value * number;
};

const double = createMultiplier(2);

console.log(double(5));
```

---

### JavaScript/05 — Arrays

This folder focuses on JavaScript arrays and commonly used array operations.

Topics include:

- Creating arrays
- Accessing array elements
- Array indexing
- Array length
- Nested arrays
- Adding and removing elements
- Sorting arrays
- Joining arrays
- Splitting strings
- Multidimensional arrays
- The spread operator

Methods explored include:

```js
.push()
.pop()
.shift()
.unshift()
.splice()
.slice()
.concat()
.join()
```

This lesson also demonstrates the difference between methods that mutate an array and methods that return a new array.

---

### JavaScript/06 — Modern Array Methods

This project focuses on modern array methods used frequently in frontend development.

Methods include:

```js
.forEach()
.map()
.filter()
.reduce()
.find()
.findIndex()
.some()
.every()
```

These methods are important because they allow data to be transformed without writing many manual loops.

For example:

```js
const numbers = [1, 2, 3, 4];

const doubled = numbers.map((number) => number * 2);

console.log(doubled);
```

The folder also covers:

- Array destructuring
- Skipping destructured values
- Default values
- Swapping variables
- Spread syntax
- Rest parameters

---

### JavaScript/07 — Objects and Immutability

This folder introduces JavaScript objects and reference values.

Topics include:

- Creating objects
- Dot notation
- Bracket notation
- Adding properties
- Updating properties
- Deleting properties
- Methods inside objects
- The `this` keyword
- `Object.keys()`
- `Object.values()`
- `Object.entries()`
- Object destructuring
- Array destructuring
- Shallow copies
- Deep copies
- `Object.seal()`
- `Object.freeze()`

Understanding references and immutability is especially important when working with React state and Redux.

---

### JavaScript/08 — How JavaScript Works

This folder contains conceptual notes rather than a normal JavaScript application.

The notes explain how JavaScript works internally, including:

- The JavaScript engine
- Single-threaded execution
- Just-in-time compilation
- Execution contexts
- The call stack
- Hoisting
- Scope
- Scope chains
- Closures

These notes are useful because they explain what happens behind the syntax used in the other projects.

---

### JavaScript/09 — `this`, `call`, `apply`, `bind`, and Prototypes

This project explores how JavaScript determines the value of `this`.

Topics include:

- Global `this`
- Strict mode
- Object methods
- Arrow functions
- Function borrowing
- `.call()`
- `.apply()`
- `.bind()`
- Prototypal inheritance
- Prototype chains
- Constructor functions
- The `new` keyword

Example:

```js
const user = {
  name: "Anshu",
};

function greet(message) {
  console.log(`${message}, ${this.name}`);
}

greet.call(user, "Hello");
```

---

### JavaScript/10 — Constructors and Classes

This folder compares traditional constructor functions with modern ES6 classes.

Topics include:

- Constructor functions
- Instance methods
- Prototypes
- ES6 classes
- Inheritance
- Method overriding
- Parent and child classes

Example:

```js
class User {
  constructor(name) {
    this.name = name;
  }

  greet() {
    return `Hello, ${this.name}`;
  }
}

class Admin extends User {
  deleteUser() {
    return "User deleted";
  }
}
```

---

### JavaScript/11 — Larger JavaScript Example

This folder contains a larger JavaScript example with HTML, CSS, and JavaScript files.

Compared with the earlier exercises, this project is structured more like a small browser application.

It can be used to practice:

- Organizing larger JavaScript files
- Connecting JavaScript with HTML
- Updating the interface dynamically
- Managing multiple UI interactions
- Combining styling and behavior

---

## DOM Projects

The `JavaScript/Dom` directory contains projects focused on the Document Object Model.

```text
JavaScript/Dom/
├── 01/
├── 02/
├── 03/
├── 04/
├── 05/
└── Works/
```

DOM manipulation allows JavaScript to interact with the HTML page after it has loaded.

Topics include:

- Selecting elements
- Changing text content
- Changing styles
- Adding event listeners
- Creating elements
- Removing elements
- Traversing the DOM
- Updating the UI based on user actions

---

## DOM Projects

The `JavaScript/Dom/Works` directory contains small practical applications.

### Bulb

An interactive bulb project that demonstrates changing the visual state of an element based on user interaction.

### MovieTiles

A movie tile interface that demonstrates creating a visual layout with HTML, CSS, and JavaScript.

### Todo

A todo-list application that demonstrates:

- Adding tasks
- Editing tasks
- Deleting tasks
- Rendering tasks dynamically
- Using SVG icons
- Managing user interactions

---

## Local Storage

The `JavaScript/LocalStorage` project demonstrates how to save data in the browser.

Local Storage allows an application to store data that remains available even after the page is refreshed.

Typical use cases include:

- Todo lists
- User preferences
- Form data
- Theme settings
- Small browser-based applications

Important Local Storage methods include:

```js
localStorage.setItem("key", "value");
localStorage.getItem("key");
localStorage.removeItem("key");
localStorage.clear();
```

---

# React

The `ReactJs` directory contains React projects created while learning component-based frontend development.

```text
ReactJs/
├── 00/
├── 01/
├── 02/
├── 03/
├── ...
├── 21/
└── Readme.md
```

There are currently numbered React learning projects from `00` through `21`.

Most of the React projects use Vite as the development server and build tool.

---

## What React Projects Teach

The React section covers:

- JSX
- Components
- Props
- State
- Event handling
- Conditional rendering
- Rendering lists
- Forms
- Reusable components
- Component composition
- Context API
- React Router
- Layouts
- Nested routes
- Protected routes
- Authentication interfaces
- API requests
- Product interfaces
- Shopping carts
- Feature organization

---

## React/00 — React Setup Experiments

The `ReactJs/00` directory contains two setup examples.

### CDN Example

The CDN example demonstrates using React directly from a CDN.

This approach does not require a complete npm project. React and ReactDOM are loaded in the HTML file, and JavaScript is used to render components.

This is useful for understanding the basic React rendering process without a build tool.

### NPM Example

The NPM example demonstrates a React project managed with npm.

To run it:

```bash
cd ReactJs/00/NPM
npm install
npm run dev
```

---

## React/01 to React/07 — React Fundamentals

The early numbered projects focus on the fundamentals of React.

Common concepts in these projects include:

- Creating components
- Passing props
- Managing component state
- Handling user events
- Rendering data
- Reusing components
- Styling React applications
- Understanding how `App.jsx` and `main.jsx` work

A typical React application has the following flow:

```text
main.jsx
   ↓
App.jsx
   ↓
Components
   ↓
Rendered user interface
```

The `main.jsx` file usually mounts the React application, while `App.jsx` acts as the main application component.

---

## React/08 — Login and Register Components

This project contains separate login and registration components.

It demonstrates:

- Component separation
- Form layout
- Reusable form structures
- Styling authentication interfaces
- Managing separate pages or views

The important idea is to keep large interfaces divided into smaller components that are easier to understand and maintain.

---

## React/09 — Component Composition

This project contains multiple components that work together.

It demonstrates how a page can be divided into smaller parts and rendered through a parent component.

Component composition allows an application to be built from reusable pieces instead of one large file.

---

## React/10 — Simple React Application

This project contains a basic React application using the standard Vite project structure.

It is useful for practicing:

- JSX
- Component rendering
- CSS
- The React entry point
- Basic project organization

---

## React/11 — Components and User Interfaces

This project includes components such as:

- A navigation bar
- A form
- A user card

It demonstrates how different components can work together to create a complete page.

---

## React/12 — Context API

This project explores the React Context API.

Context allows data to be shared across components without manually passing props through every level of the component tree.

The project includes:

- Multiple components
- A context provider
- Shared values
- Context-based data access

Context is useful for values such as:

- Theme settings
- User information
- Authentication state
- Language preferences
- Application settings

---

## React/13 — Multiple Pages and Components

This project contains separate home and about components.

It introduces the idea of organizing an application into different page-level components.

---

## React/14 — Product and Cart Interface

This project contains product-related components and a shopping cart.

It demonstrates:

- Product cards
- Navigation
- Product data
- Cart state
- Context API
- Reusable components
- Shared application state

This is an example of how multiple components can work together to build a small e-commerce interface.

---

## React/15 — Routing and Pages

This project introduces React Router concepts.

It includes:

- Home page
- About page
- Contact page
- Details page
- Navigation
- Route configuration

Routing allows a React application to display different pages based on the URL without requiring a full browser reload.

---

## React/16 — Products and Protected Routes

This project expands on routing, products, and application state.

It includes:

- Product pages
- Product details
- About page
- Navigation
- Context API
- Protected routes
- Route-based layouts

Protected routes are used to restrict access to pages based on a condition, such as whether a user is logged in.

---

## React/17 — Layout-Based Application Structure

This project introduces layouts.

It includes:

- A main layout
- Navigation
- Home page
- About page
- Services page
- Route configuration

Layouts are useful when multiple pages share common UI elements such as navigation bars, headers, or footers.

---

## React/18 — Authentication and API-Based Interface

This is one of the more advanced React projects in the repository.

It includes:

- Authentication pages
- Login and registration
- User pages
- Product pages
- API configuration
- Authentication context
- Custom authentication hooks
- Protected routes
- Main layout
- Authentication layout
- Reusable form components
- Product and user cards

The project demonstrates how a React application can be organized into separate layers:

```text
Pages
   ↓
Components
   ↓
Hooks and Context
   ↓
API Configuration
```

---

## React/19 — Component and Page Structure

This project contains separate home and about components.

It also includes a diagram file for planning or explaining the application.

---

## React/20 — React Starter Project

This project contains a simple Vite React application.

It can be used for experimenting with:

- React components
- JSX
- CSS
- Basic project setup
- Application entry points

---

## React/21 — API and Layout Experiment

This project includes:

- API functions
- A navigation bar
- A main layout
- Home page
- About page
- Contact page
- Route configuration

It demonstrates how API code, pages, layouts, and routes can be separated into different directories.

---

# Redux Toolkit

The `ReduxToolkit` directory contains projects focused on global state management with Redux Toolkit.

```text
ReduxToolkit/
├── 01/
├── 02/
├── 03/
├── 04/
├── 05/
└── Readme.md
```

Redux Toolkit simplifies Redux by providing tools such as:

- `configureStore`
- `createSlice`
- Generated action creators
- Reducers
- Centralized state
- Redux DevTools support
- Async logic patterns

---

## Why Redux Toolkit Is Used

React state is useful when data belongs to one component or a small group of components.

However, some data needs to be accessed by many parts of an application.

Examples include:

- Authenticated user information
- Shopping cart items
- Product data
- Orders
- Application settings

Redux Toolkit provides a central store where this shared state can be managed.

---

## Redux Toolkit/01 — Counter and Store Basics

The first Redux Toolkit project introduces the basic Redux flow.

It includes:

- A Redux store
- A counter slice
- Increment actions
- Decrement actions
- `useSelector`
- `useDispatch`

The general flow is:

```text
User clicks a button
        ↓
Component dispatches an action
        ↓
Reducer updates the state
        ↓
React reads the new state
        ↓
UI updates
```

---

## Redux Toolkit/02 — Authentication State

This project introduces authentication-related state management.

It contains examples involving:

- Authentication slices
- Login pages
- Registration pages
- Authenticated layouts
- Public layouts
- Protected routes
- Custom authentication hooks

The project demonstrates how login state can be shared throughout the application.

---

## Redux Toolkit/03 — Products and API Requests

This project combines Redux Toolkit with product data and API requests.

It includes:

- Product API functions
- Product hooks
- Product cards
- Product filters
- Loading skeletons
- Authentication
- Protected routes
- Shop pages

This project demonstrates how global state management can be combined with remote data.

---

## Redux Toolkit/04 — Feature-Based Architecture

This is a more structured Redux Toolkit application.

The project separates features into their own directories:

```text
src/
├── features/
│   ├── auth/
│   ├── cart/
│   ├── orders/
│   └── products/
├── shared/
├── app/
├── config/
└── routes/
```

This style is useful for larger applications because each feature can contain its own:

- API logic
- Hooks
- State
- Components
- Pages

The project includes examples involving:

- Authentication
- Products
- Cart functionality
- Orders
- Protected routes
- Shared navigation
- API configuration
- Feature-specific pages

---

## Redux Toolkit/05 — API and Data Fetching Experiments

This project contains experiments involving:

- Product API calls
- Product cards
- Infinite loading
- TanStack-related functionality
- Reusable components
- API-based rendering

It demonstrates how frontend applications can request and display data from an external API.

---

## Redux Toolkit Concepts

### Store

The store contains the application’s global state.

```js
import { configureStore } from "@reduxjs/toolkit";

export const store = configureStore({
  reducer: {
    counter: counterReducer,
  },
});
```

### Slice

A slice contains:

- Initial state
- Reducers
- Action creators

```js
const counterSlice = createSlice({
  name: "counter",
  initialState: {
    value: 0,
  },
  reducers: {
    increment: (state) => {
      state.value += 1;
    },
  },
});
```

### `useSelector`

`useSelector` reads data from the Redux store.

```js
const count = useSelector((state) => state.counter.value);
```

### `useDispatch`

`useDispatch` sends actions to the store.

```js
const dispatch = useDispatch();

dispatch(increment());
```

---

## Authentication and Protected Routes

Several projects include public and protected routes.

### Public Routes

Public routes are pages available to users who are not logged in.

Examples include:

- Login
- Registration
- Landing pages

### Protected Routes

Protected routes are pages available only after authentication.

Examples include:

- Home dashboard
- Product pages
- Cart
- Orders
- User pages

A protected route commonly checks authentication state and redirects the user when necessary.

---

## Local Storage and Redux Hydration

Redux state is stored in memory, which means it is reset when the page is refreshed.

To preserve important data, the projects can use Local Storage.

A typical process is:

```text
User logs in
    ↓
User data is saved to Local Storage
    ↓
Redux state is updated
    ↓
Page is refreshed
    ↓
User data is loaded from Local Storage
    ↓
Redux state is restored
```

This restoration process is often called hydration.

---

# TypeScript

The `TypeScript` directory contains TypeScript fundamentals and React projects written with TypeScript.

```text
TypeScript/
├── 01/
├── 02/
├── 03/
└── Readme.md
```

---

## What TypeScript Projects Teach

The TypeScript projects cover:

- Type annotations
- Type inference
- Primitive types
- Object types
- Interfaces
- Optional properties
- Function parameter types
- Function return types
- Callback types
- Rest parameters
- Declaration files
- TypeScript compiler output
- React with TypeScript
- Typed component props
- Typed API data
- Typed React state
- Vite TypeScript configuration

---

## TypeScript/01 — TypeScript Fundamentals

This project introduces the TypeScript workflow.

It includes:

- TypeScript source files
- Compiled JavaScript files
- Declaration files
- Source maps
- `tsconfig.json`
- Learning diagrams

Important files include:

```text
index.ts
index.js
index.d.ts
tsconfig.json
```

The general workflow is:

```text
TypeScript source
        ↓
TypeScript compiler
        ↓
JavaScript output
        ↓
Browser or Node.js
```

TypeScript is not executed directly by the browser. It is usually compiled into JavaScript first.

---

## TypeScript/02 — Types and Functions

This project explores more advanced TypeScript functions and object structures.

Topics include:

- Object type definitions
- Nested objects
- Optional properties
- Function parameters
- Return types
- Callbacks
- Functions returning functions
- Currying
- Rest parameters
- Typed `reduce()`
- Running TypeScript directly with `tsx`
- Development with `nodemon`

Example:

```ts
type User = {
  name: string;
  age: number;
  company: string;
  address: {
    city: string;
    state: string;
  };
  employeeId?: string;
};
```

The `?` means that `employeeId` is optional.

---

## TypeScript/03 — React with TypeScript

This project combines React, TypeScript, Vite, and API requests.

It includes:

- React components written in `.tsx`
- Typed product data
- A reusable `Product` interface
- API requests
- Typed props
- Product cards
- Vite configuration
- ESLint configuration

The data flow looks like this:

```text
API request
    ↓
App.tsx
    ↓
Product[]
    ↓
ProductCard.tsx
    ↓
Product interface
    ↓
Rendered product UI
```

Example product interface:

```ts
export interface Product {
  id: number;
  title: string;
  category: string;
  image: string;
  price: number;
  description: string;
  rating: {
    rate: number;
    count: number;
  };
}
```

This interface describes the structure of a product returned from the API.

---

## TypeScript Concepts

### Type Annotations

Type annotations explicitly define the type of a value.

```ts
let username: string = "developer";
let age: number = 25;
let isLoggedIn: boolean = true;
```

### Function Types

Function parameters and return values can be typed.

```ts
const multiply = (a: number, b: number): number => {
  return a * b;
};
```

### Optional Properties

Optional properties use the `?` symbol.

```ts
type User = {
  name: string;
  email?: string;
};
```

### Arrays

Arrays can be typed in multiple ways.

```ts
const numbers: number[] = [1, 2, 3];

const names: Array<string> = ["Anshu", "Developer"];
```

### Typed React State

React state can be given a specific type.

```tsx
const [products, setProducts] = useState<Product[]>([]);
```

### Typed Component Props

Component props can also be typed.

```tsx
type ProductCardProps = {
  product: Product;
};

const ProductCard = ({ product }: ProductCardProps) => {
  return <h2>{product.title}</h2>;
};
```

Typed props help TypeScript detect missing or incorrectly shaped data.

---

# How to Run the Projects

The repository contains independent projects, so dependencies are installed inside the specific project directory you want to use.

---

## Running a Vanilla JavaScript Project

Most JavaScript projects contain:

```text
index.html
script.js
style.css
```

You can open the `index.html` file directly in a browser.

For example:

```text
JavaScript/01/index.html
```

For projects that require a local server, use one of the following options.

### Using Python

From the repository root:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

### Using `serve`

```bash
npx serve JavaScript/01
```

### Using VS Code Live Server

You can also install the Live Server extension in Visual Studio Code and open the project's `index.html` file with it.

---

## Running a React Project

Move into the selected React project:

```bash
cd ReactJs/01
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

The terminal will display a local URL, usually similar to:

```text
http://localhost:5173
```

The exact commands can vary, so check the project's `package.json` file.

---

## Running a Redux Toolkit Project

```bash
cd ReduxToolkit/01
npm install
npm run dev
```

You can replace `01` with another Redux Toolkit project number.

For example:

```bash
cd ReduxToolkit/04
npm install
npm run dev
```

---

## Running a TypeScript Project

For the TypeScript projects:

```bash
cd TypeScript/01
npm install
npm run dev
```

For the React TypeScript project:

```bash
cd TypeScript/03
npm install
npm run dev
```

---

# Common Commands

## Clone the Repository

```bash
git clone https://github.com/anshuxthakor/Frontend.git
```

## Enter the Repository

```bash
cd Frontend
```

## Install Dependencies

```bash
npm install
```

## Start a Development Server

```bash
npm run dev
```

## Build a Project

```bash
npm run build
```

## Preview a Production Build

```bash
npm run preview
```

## Run ESLint

```bash
npm run lint
```

## Compile TypeScript

```bash
npx tsc
```

## Check TypeScript Without Generating Files

```bash
npx tsc --noEmit
```

## Run a TypeScript File Using TSX

```bash
npx tsx index.ts
```

The commands available in each project depend on its individual `package.json` file.

---

# Recommended Learning Order

A useful way to go through this repository is:

```text
JavaScript/01
    ↓
JavaScript/02
    ↓
JavaScript/03
    ↓
JavaScript/04
    ↓
JavaScript/05
    ↓
JavaScript/06
    ↓
JavaScript/07
    ↓
JavaScript/Dom
    ↓
JavaScript/LocalStorage
    ↓
ReactJs/00
    ↓
ReactJs/01 - ReactJs/21
    ↓
ReduxToolkit/01
    ↓
ReduxToolkit/02 - ReduxToolkit/05
    ↓
TypeScript/01
    ↓
TypeScript/02
    ↓
TypeScript/03
```

This order moves from basic language concepts toward complete application architecture.

---

# Learning Method

When studying a project, use the following process:

1. Open the project folder.
2. Read the HTML or React entry file first.
3. Identify where the application starts.
4. Read the JavaScript, JSX, or TypeScript logic.
5. Check how data moves through the application.
6. Run the project in the browser.
7. Open the browser developer tools.
8. Change one small part of the code.
9. Refresh the page and observe the result.
10. Try rebuilding the example without looking at the original code.

For React and Redux projects, follow the data flow:

```text
Component
    ↓
Event handler
    ↓
State update or dispatched action
    ↓
Reducer, context, or hook
    ↓
Updated state
    ↓
Re-rendered UI
```

---

# Learning Tips

## For JavaScript

- Use the browser console frequently.
- Predict the output before running the code.
- Try changing `var` to `let` or `const`.
- Compare mutating and non-mutating array methods.
- Practice writing the same solution with a loop and with array methods.
- Experiment with `this`, closures, and prototypes.

## For DOM Projects

- Inspect the HTML structure before reading the JavaScript.
- Identify which elements are selected.
- Find the event listeners.
- Check what changes when an event is triggered.
- Use browser developer tools to inspect styles and elements.

## For React

- Start by understanding `main.jsx` and `App.jsx`.
- Identify the component tree.
- Check which components receive props.
- Find where state is stored.
- Trace the event that changes the state.
- Use React Developer Tools to inspect props and state.

## For Redux Toolkit

- Start with the store.
- Read each slice.
- Identify the initial state.
- Find the actions.
- Search for `useSelector`.
- Search for `useDispatch`.
- Follow the path from a button click to the reducer.

## For TypeScript

- Read the type definitions before reading the components.
- Try changing a type and observe the compiler error.
- Avoid using `any` unless it is necessary.
- Use interfaces and type aliases to describe data.
- Run `npx tsc --noEmit` to check your code.

---

# Project Organization

The projects use several different structures because this repository documents the learning process.

Some projects are simple:

```text
project/
├── index.html
├── script.js
└── style.css
```

React projects usually follow a structure similar to:

```text
project/
├── public/
├── src/
│   ├── App.jsx
│   ├── main.jsx
│   ├── components/
│   ├── pages/
│   ├── layouts/
│   └── routes/
├── package.json
└── vite.config.js
```

More advanced applications may use a feature-based structure:

```text
src/
├── app/
├── config/
├── features/
│   ├── auth/
│   ├── products/
│   ├── cart/
│   └── orders/
├── shared/
├── layouts/
├── pages/
└── routes/
```

The feature-based structure keeps related code together and makes larger projects easier to maintain.

---

# Notes About the Repository

- Projects are independent from one another.
- Not every project is intended to be production-ready.
- Some code is written specifically to demonstrate one concept.
- Some folders contain notes, diagrams, or generated files.
- Some projects may use external APIs.
- External APIs may change or become unavailable.
- Dependency versions may differ between projects.
- Always check the individual `package.json` before running commands.
- The repository is updated as new topics are learned.

---

# Future Improvements

Possible future improvements include:

- Adding a README file to every numbered project.
- Adding screenshots for completed projects.
- Adding live demo links.
- Adding project difficulty labels.
- Adding project descriptions to each folder.
- Adding automated tests.
- Adding loading and error states to API projects.
- Adding environment variable documentation.
- Adding more TypeScript examples.
- Adding unit tests with Vitest.
- Adding form validation.
- Adding API error handling.
- Adding deployment instructions.
- Adding a root-level project index.
- Adding a license file.
- Adding reusable configuration files.
- Adding shared components between projects where appropriate.

---

# Contributing

This repository is mainly a personal learning workspace, but suggestions and improvements are welcome.

If you want to contribute:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Test the relevant project.
5. Add or update documentation when necessary.
6. Open a pull request.

When adding a new project:

- Put it in the appropriate technology directory.
- Use a clear folder name.
- Keep the project focused on a specific concept.
- Include a `README.md` if the project is complex.
- Explain how to run the project.
- Document required environment variables.
- Avoid committing `node_modules`.
- Add comments for difficult concepts.

---

# License

No license has currently been added to this repository.

Until a license is added, the code should be treated as personal learning material. Reuse, modification, or redistribution should not be assumed to be permitted.

---

# Author

Created and maintained by [anshuxthakor](https://github.com/anshuxthakor).

---

# Repository Link

[https://github.com/anshuxthakor/Frontend](https://github.com/anshuxthakor/Frontend)
