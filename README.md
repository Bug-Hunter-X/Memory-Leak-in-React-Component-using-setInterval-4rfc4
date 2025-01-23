# React setInterval Memory Leak

This repository demonstrates a common error in React components: using `setInterval` within `useEffect` without proper cleanup. This leads to memory leaks and unexpected behavior.

## Bug Description
The `MyComponent` component uses `setInterval` to update the count every second. However, it fails to clear the interval when the component unmounts, causing a memory leak.

## Solution
The solution involves using the return value of `useEffect` to clear the interval when the component unmounts.