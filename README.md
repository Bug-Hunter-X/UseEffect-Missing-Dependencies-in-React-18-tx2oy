# React 18 useEffect Bug: Missing Dependencies

This repository demonstrates a common bug in React 18 related to the `useEffect` hook and missing dependencies in its dependency array.  This can lead to unexpected behavior and difficult-to-debug issues. 

## The Problem
The `bug.js` file contains a component that uses `useEffect` to update a counter every second. However, the dependency array is empty (`[]`), meaning the effect will only run once after the initial render.  This leads to the counter not updating.

## The Solution
The `bugSolution.js` file demonstrates the correct implementation where the `count` state variable is included in the dependency array. Now, the effect will run whenever the `count` variable changes, ensuring the counter updates correctly.

## How to reproduce the bug:
1. Clone this repository.
2. Run `npm install` to install dependencies (if needed).
3. Run `npm start` (or your preferred start script) to start the application.
4. Observe that the counter in the `bug.js` component does not increment, while the counter in `bugSolution.js` works correctly. 