# TypeScript — Learning Projects, Exercises & React Examples

This directory contains my TypeScript learning exercises, notes, experiments, and React projects.

The examples start with basic TypeScript syntax and gradually move toward using TypeScript with React, Vite, API requests, typed component props, interfaces, and reusable data models.

---

## Table of contents

- [Quick start](#quick-start)
- [What you’ll learn](#what-youll-learn)
- [Folder index](#folder-index)
- [TypeScript concepts covered](#typescript-concepts-covered)
- [TypeScript with React](#typescript-with-react)
- [Learning tips](#learning-tips)
- [Suggested improvements](#suggested-improvements)

---

## Quick start

The folders contain separate learnings. Open the folder you want to practice.

### TypeScript 01

```bash
cd TypeScript/01
npm install
npm run dev
```

This project focuses on the fundamentals of TypeScript and includes compiled JavaScript output and TypeScript declaration files.

### TypeScript 02

```bash
cd TypeScript/02
npm install
npm run dev
```

This project contains TypeScript functions, object types, optional properties, callbacks, currying, rest parameters, and return type annotations.

### TypeScript 03

```bash
cd TypeScript/03
npm install
npm run dev
```

This is a Vite + React + TypeScript project. It fetches product data from an API and displays the products using typed React components.

---

## What you’ll learn

This section focuses on:

- TypeScript primitive types
- Type annotations
- Type inference
- Function parameter and return types
- Object types
- Interfaces
- Optional properties
- Arrays and rest parameters
- Callback functions
- Generic concepts
- TypeScript declaration files
- TypeScript compiler configuration
- React components written with `.tsx`
- Typed component props
- Typed state with `useState`
- API data models
- Type-safe data rendering
- Vite and TypeScript project configuration

---

## Folder index

### 01 — TypeScript fundamentals

The first project introduces the basic TypeScript workflow.

Topics include:

- Writing TypeScript in an `index.ts` file
- Compiling TypeScript into JavaScript
- Understanding generated `.js` files
- Understanding generated `.d.ts` declaration files
- Reading TypeScript compiler output
- Using `tsconfig.json`
- Exploring TypeScript concepts with notes and diagrams

This folder is useful for understanding how TypeScript code is transformed before it runs in JavaScript.

---

### 02 — Types, functions and advanced function patterns

This project contains practical examples of TypeScript types and functions.

Topics include:

- Object type definitions
- Nested object types
- Optional properties
- Function parameter types
- Function return types
- Callback functions
- Functions returning functions
- Currying
- Rest parameters
- The `reduce` method with typed values
- Running TypeScript directly with `tsx`
- Using `nodemon` during development

Example concepts:

```ts
type UserObj = {
  name: string;
  age: number;
  company: string;
  address: {
    street: string;
    city: string;
    state: string;
  };
  employeeId?: string;
};
```

```ts
const sum = (...numbers: number[]): number => {
  return numbers.reduce((total, value) => total + value, 0);
};
```

---

### 03 — React with TypeScript

This project demonstrates how TypeScript can be used inside a React application created with Vite.

The application:

- Uses React and TypeScript
- Fetches products from the Fake Store API
- Stores API data using typed React state
- Defines a reusable `Product` interface
- Passes typed props to components
- Renders reusable product cards
- Uses Axios for API requests
- Uses Vite as the development server
- Uses ESLint for code quality

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
Product UI
```

The product model is defined in `src/types.ts`:

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

The `ProductCard` component receives a typed product prop:

```tsx
const ProductCard = ({ product }: { product: Product }) => {
  return <h2>{product.title}</h2>;
};
```

This makes the component safer because TypeScript can check that the required product properties exist.

---

## TypeScript concepts covered

### Type annotations

Type annotations explicitly describe the type of a value.

```ts
let username: string = "developer";
let age: number = 25;
let isLoggedIn: boolean = true;
```

### Function types

Parameters and return values can be typed.

```ts
const multiply = (a: number, b: number): number => {
  return a * b;
};
```

### Object types

Object structures can be described with a type or interface.

```ts
type User = {
  name: string;
  age: number;
};
```

### Optional properties

A property can be marked as optional using `?`.

```ts
type User = {
  name: string;
  email?: string;
};
```

### Arrays

Arrays can be typed using either syntax:

```ts
const numbers: number[] = [1, 2, 3];
const names: Array<string> = ["A", "B", "C"];
```

### Rest parameters

Rest parameters allow a function to accept multiple values of the same type.

```ts
const add = (...values: number[]): number => {
  return values.reduce((total, value) => total + value, 0);
};
```

### Interfaces

Interfaces are useful for describing reusable object shapes.

```ts
interface Product {
  id: number;
  title: string;
  price: number;
}
```

### Typed React state

React state can be given an explicit type.

```tsx
const [products, setProducts] = useState<Product[]>([]);
```

### Typed component props

Component props can be typed to make reusable components safer.

```tsx
type ProductCardProps = {
  product: Product;
};

const ProductCard = ({ product }: ProductCardProps) => {
  return <div>{product.title}</div>;
};
```

---

## TypeScript with React

The `03` project demonstrates a common TypeScript React architecture:

```text
src/
├── App.tsx
├── main.tsx
├── types.ts
├── index.css
└── components/
    └── ProductCard.tsx
```

### `App.tsx`

Responsible for:

- Fetching product data
- Storing the response in state
- Passing each product to the product card component

### `types.ts`

Responsible for:

- Defining the structure of product data
- Keeping data models reusable
- Making API-related code easier to understand

### `ProductCard.tsx`

Responsible for:

- Receiving one typed product
- Rendering product information
- Keeping the UI component reusable

### `main.tsx`

Responsible for:

- Finding the root DOM element
- Mounting the React application

---

## Useful commands

### Run a TypeScript project

```bash
npm run dev
```

### Install dependencies

```bash
npm install
```

### Compile TypeScript

```bash
npx tsc
```

### Run a file with TSX

```bash
npx tsx index.ts
```

### Check TypeScript without generating files

```bash
npx tsc --noEmit
```

### Build the React project

```bash
npm run build
```

### Run ESLint

```bash
npm run lint
```

---

## Learning tips

- Start with the `01` folder to understand the TypeScript workflow.
- Practice changing types and observe the compiler errors.
- Read the `02` folder to understand functions and object types.
- Use `npx tsc --noEmit` to check your code without creating output files.
- Study `src/types.ts` in the `03` project before reading the React components.
- Try adding new properties to the `Product` interface.
- Create a new component that receives typed props.
- Add loading and error states to the API request.
- Use optional properties when an API value may not always exist.
- Avoid using `any` unless there is a strong reason to use it.
- Use meaningful names for interfaces, types, functions, and variables.

---

## Suggested improvements

Future TypeScript projects can include:

- Union and intersection types
- Literal types
- Enums
- Generics
- Type guards
- Utility types such as `Partial`, `Pick`, `Omit`, and `Record`
- Type-safe forms
- Custom React hooks with TypeScript
- Typed React Context
- Error and loading state handling
- Axios response types
- API service files
- Type-safe routing
- TypeScript with Redux Toolkit
- Unit testing with Vitest
- Runtime validation with Zod

---

## Contribution guidelines

When adding a new TypeScript example:

- Create a separate numbered folder.
- Add a short explanation of the topic.
- Include a `README.md` or notes file when the example becomes complex.
- Keep each project focused on one concept.
- Use strict TypeScript settings where possible.
- Add comments explaining difficult concepts.
- Include the commands required to run the example.
- Avoid committing unnecessary generated files such as `node_modules`.
- Use descriptive names for larger projects.

---

## License and contact

This repository is a personal learning repository containing TypeScript exercises, experiments, and frontend projects.

Repository owner: [anshuxthakor](https://github.com/anshuxthakor)