# useParams Hook in React Router v6 Returns Undefined Conditionally

This repository demonstrates a common issue with the `useParams` hook in React Router v6:  returning undefined values when used within conditionally rendered components or during server-side rendering (SSR).  The problem arises because the route parameters are not immediately available, and accessing them before mounting can lead to undefined values or errors.

The `bug.js` file illustrates the problematic code, and `bugSolution.js` demonstrates a solution using conditional rendering and the `useEffect` hook.

## Problem
The `useParams` hook in React Router Dom v6 needs to be accessed after the component has fully mounted and the route has been matched. Accessing `useParams` before this leads to undefined values.