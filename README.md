# React useEffect Hook Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook: infinite loops.  The bug occurs when the `useEffect` hook lacks a proper dependency array or contains incorrect dependencies, leading to the effect running repeatedly, potentially causing performance issues or application crashes.

## Bug Description
The provided `bug.js` file contains a `MyComponent` component that uses the `useEffect` hook to log the current value of a state variable (`count`) to the console.  However, because the dependency array `[count]` is missing, the effect runs on every render, causing the `count` to constantly update and triggering the effect again, resulting in an infinite loop. 

## Solution
The `bugSolution.js` file provides a corrected version of the component. By including `[count]` in the dependency array, the `useEffect` hook now only runs when the `count` variable changes. 