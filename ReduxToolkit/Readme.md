# Redux Toolkit — Demos, Exercises & Notes

This directory contains my Redux Toolkit learning projects, experiments, and notes while building React applications with centralized state management.

The examples here explore how Redux Toolkit simplifies Redux with `configureStore`, `createSlice`, reducers, actions, selectors, and async logic. In this folder, I also use React Router, react-hook-form, localStorage, and protected routes to build a more realistic app flow.

Use this README as a starting point to understand what the Redux Toolkit section covers and how the examples are organized.

---

## Table of contents

- Quick start
- What you’ll learn here
- Folder index
- Core Redux Toolkit concepts
- App flow overview
- Authentication and route protection
- Hydration and localStorage
- Learning tips
- Suggested improvements

---

## Quick start

1. Open any subfolder inside `ReduxToolkit/`.
2. Install dependencies if needed:
   ```bash
   npm install
   ```
3. Start the app:
   ```bash
   npm run dev
   ```
4. Open the local URL shown in the terminal.
5. Read the related source files side by side with this README to connect the concepts with the implementation.

---

## What you’ll learn here

This section is mainly focused on:

- setting up a Redux store
- creating slices with Redux Toolkit
- updating and reading global state
- dispatching actions from React components
- protecting routes based on authentication state
- persisting user data with localStorage
- hydrating Redux state after refresh
- combining Redux with React Router and forms

---

## Folder index

The `ReduxToolkit/` directory contains multiple mini-projects and learning stages.

### 01 — Counter example
A very small Redux Toolkit starter project.

What it demonstrates:
- `configureStore`
- a simple slice
- increment and decrement actions
- `useSelector` to read the counter value
- `useDispatch` to trigger updates from buttons

Best for:
- understanding the absolute basics of Redux Toolkit
- learning the relationship between store, slice, and component

---

### 02 — Redux Toolkit practice notes
This folder appears to contain notes and learning material around Redux Toolkit concepts.

What it may include:
- slice structure
- reducer logic
- state updates
- basic Redux Toolkit examples

Best for:
- revision
- quick concept review
- experimenting with state management patterns

---

### 03 — Authentication example
A more advanced example focused on user authentication and protected routes.

What it demonstrates:
- auth state stored in Redux
- `addUser` / `removeUser` actions
- login and registration forms
- route guards using `PublicProtected`
- reading and writing from `localStorage`
- hydration of user state on refresh

This example shows how Redux Toolkit can be used for application-wide auth flow instead of keeping everything inside local component state.

---

### 04 — E-commerce layered architecture
A more structured app setup using Redux Toolkit with React Router and other supporting libraries.

What it demonstrates:
- layered folder organization
- protected route layouts
- store hydration during app start
- auth actions and auth state
- feature-based structure
- better separation of concerns

Best for:
- understanding how Redux Toolkit scales in a larger app
- learning a feature-based architecture
- seeing Redux used in a real application style

---

## Core Redux Toolkit concepts

### 1. Store setup

Redux Toolkit usually starts with `configureStore()`.

Example:

```js
import { configureStore } from "@reduxjs/toolkit";
import counterReducer from "../features/counter/counterSlice";

export const store = configureStore({
  reducer: {
    counter: counterReducer,
  },
});
```

The store is the global state container for the app.  
Each key in the reducer object becomes a slice of state.

For example:

- `store.counter`
- `store.auth`

---

### 2. Slices

A slice bundles:
- initial state
- reducer logic
- auto-generated action creators

Example:

```js
import { createSlice } from "@reduxjs/toolkit";

const authSlice = createSlice({
  name: "auth",
  initialState: {
    user: null,
    isAuthenticated: false,
  },
  reducers: {
    addUser: (state, action) => {
      state.user = action.payload;
      state.isAuthenticated = true;
    },
    removeUser: (state) => {
      state.user = null;
      state.isAuthenticated = false;
    },
  },
});
```

Why slices are useful:
- less boilerplate than classic Redux
- related state and logic live together
- actions and reducers are generated in one place

---

### 3. Actions and reducers

Reducers describe how state changes when an action is dispatched.

With Redux Toolkit, reducers are often written in a mutation-like style:

```js
state.user = action.payload;
```

This is safe because Redux Toolkit uses Immer internally, so the final update remains immutable under the hood.

---

### 4. Reading state with `useSelector`

`useSelector` lets a React component read data from the store.

Example:

```js
const { user } = useSelector((store) => store.auth);
```

This means:
- the component subscribes to `store.auth`
- it re-renders when that state changes
- you do not need to pass props through many component layers

---

### 5. Updating state with `useDispatch`

`useDispatch` lets a component send actions to the store.

Example:

```js
const dispatch = useDispatch();
dispatch(addUser(loggedInUser));
```

This is how React components trigger Redux updates.

---

## App flow overview

A typical Redux Toolkit flow in this folder looks like this:

1. User opens the app
2. App loads Redux store
3. Components read state using `useSelector`
4. User submits a form or clicks a button
5. Component dispatches an action
6. Slice reducer updates the store
7. UI re-renders with the new state

This pattern keeps business logic centralized and the UI easier to reason about.

---

## Authentication and route protection

In the auth examples, Redux Toolkit is used to store login state and control access to pages.

### PublicProtected
Used for routes like:
- login
- register

If the user is already authenticated, they are redirected away from the public pages.

### MainProtected
Used for routes like:
- home
- product pages
- cart
- orders

If the user is not authenticated, they are redirected back to the login page.

This keeps the app secure at the routing level.

---

## Hydration and localStorage

Some examples persist the logged-in user in `localStorage` so refreshes do not wipe the session immediately.

Typical hydration flow:

1. User logs in
2. User object is stored in `localStorage`
3. Redux store is updated
4. On app load, stored user data is read back
5. Redux is hydrated again from `localStorage`

This is important because Redux state resets on refresh unless you restore it manually.

---

## Learning tips

- Start with the simplest example first.
- Trace one feature from UI → action → reducer → store → UI.
- Compare classic Redux ideas with Redux Toolkit shortcuts.
- Inspect the auth flow carefully if you want to understand real app state management.
- Try adding one extra field to the store and wiring it into a component.

---

## Suggested improvements

If this section grows, good next steps could be:

- add a dedicated README for each subfolder
- document the file structure for every example
- include screenshots of the UI
- add a concept map for Redux Toolkit architecture
- explain async logic with `createAsyncThunk`
- add a persistence section for `localStorage` or session storage

---

## Closing note

This folder is meant as a learning space, so the best way to use it is to read the code, run the examples, and connect the Redux Toolkit concepts with the UI behavior you see in the browser.