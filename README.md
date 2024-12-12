# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency array.  The `useEffect` hook, without a dependency array, runs after every render, creating a loop.

## Bug Description
The provided `MyComponent` uses `useEffect` to log the `count` value.  However, because the dependency array is missing, the effect runs after every render.  Each run updates the `count`, triggering another render, leading to an infinite loop and console spam.

## Solution
The solution involves adding the `count` variable to the dependency array.  This ensures the effect only runs when the `count` changes, preventing the infinite loop.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite loop in the browser's console and the unusually fast updates to the counter.
