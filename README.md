# React 19 useEffect Hook Bug

This repository demonstrates a common bug in React 19 applications involving the `useEffect` hook.  The bug occurs when a dependency is missing from the `useEffect` dependency array, leading to an infinite rendering loop.

## Bug Description
The `useEffect` hook in the `bug.js` file is missing the `count` variable in its dependency array. This causes the effect to run on every render, triggering a state update which, in turn, triggers another render, creating an infinite loop.

## Solution
The solution, provided in `bugSolution.js`, is to include `count` in the dependency array.  This ensures the effect only runs when the `count` value changes.

## How to reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the infinite rendering loop in the console (in `bug.js`)
5. Replace `bug.js` with `bugSolution.js` and re-run to see the fix.

This example highlights the importance of carefully considering the dependencies you include in the `useEffect` hook's dependency array to avoid unexpected behavior.