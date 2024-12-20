# React useEffect Hook Missing Dependency
This repository demonstrates a common error in React: forgetting to include necessary dependencies in the `useEffect` hook's dependency array. This can lead to unexpected behavior, such as infinite re-renders or stale closures.

## Problem
The initial `bug.js` code has a `useEffect` hook without the `count` variable in the dependency array. This means the effect runs after every render, even if `count` hasn't changed. In this case, this creates an infinite loop, causing the component to continuously update and log to the console.

## Solution
The `bugSolution.js` file fixes the issue by including `count` in the dependency array. Now, the effect only runs when `count` changes, preventing the infinite loop and ensuring the correct behavior.

## How to Run
1. Clone this repository.
2. Navigate to the project directory in your terminal.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.