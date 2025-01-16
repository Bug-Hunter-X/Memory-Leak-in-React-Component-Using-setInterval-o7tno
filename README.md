# React UseEffect Cleanup Bug

This repository demonstrates a common bug in React components that use the `useEffect` hook with `setInterval` without proper cleanup. This leads to memory leaks and unexpected behavior.

## Bug Description
The `MyComponent` component uses `setInterval` to update a counter every second.  However, it is missing the cleanup function in the `useEffect` hook, meaning that the interval continues to run even after the component unmounts, causing a memory leak.

## Solution
The solution involves adding a cleanup function to the `useEffect` hook. This function is executed when the component unmounts or when the dependencies change, ensuring that the `setInterval` is cleared, preventing memory leaks.