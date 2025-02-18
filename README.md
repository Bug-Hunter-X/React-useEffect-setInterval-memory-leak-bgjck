# React useEffect setInterval Memory Leak
This example demonstrates a common error in React components: using `setInterval` within `useEffect` without proper cleanup. This can lead to memory leaks and unexpected behavior.

## Problem
The `MyComponent` uses `setInterval` to update the count every second. However, the interval is never cleared.  This means that even when the component unmounts, the interval continues to run, potentially causing a memory leak and unnecessary updates.

## Solution
The solution involves using the cleanup function provided by `useEffect` to clear the interval when the component unmounts or when the dependencies change.
