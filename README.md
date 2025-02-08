# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications: an infinite loop caused by incorrectly updating state within a useEffect hook's dependency array.

## The Bug

The `bug.js` file contains a component that attempts to increment a state variable (`count`) within its useEffect hook.  Because the `count` variable is itself a dependency of useEffect, every update to `count` will cause a re-render, leading to an infinite loop of state updates.

## The Solution

The `bugSolution.js` file provides a corrected version.  The key change is removing the `count` variable from the dependency array.  This ensures the useEffect runs only once after the initial render, preventing the infinite loop.  Alternatively, you could introduce a condition to break the loop. 

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`. Observe the infinite loop. Run the solution to see the fix.