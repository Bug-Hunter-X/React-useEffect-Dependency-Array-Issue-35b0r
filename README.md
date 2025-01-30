# React useEffect Dependency Array Issue

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include state variables in the dependency array.  This can lead to unexpected behavior, such as infinite re-renders or stale closures.

## Bug Description

The `bug.js` file contains a component that increments a counter.  However, the `useEffect` hook is missing the `count` variable in its dependency array. This causes the effect to run after every render, regardless of whether the `count` value has changed, resulting in an infinite loop of console logs.

## Solution

The `bugSolution.js` file shows the corrected code. The `count` variable is added to the dependency array.  Now, the effect only runs when the `count` value changes, fixing the infinite loop.

## How to Run

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install`.
4. Run `npm start`.

Observe the console logs in both versions to understand the difference.