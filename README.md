# React SetInterval Memory Leak

This repository demonstrates a common error in React: using `setInterval` within a `useEffect` hook without proper cleanup. This leads to a memory leak and unpredictable component behavior.

## The Bug
The `bug.js` file shows the problematic code.  The `setInterval` function is used to update the count every second. However, the lack of a cleanup function in the `useEffect` means that the interval continues to run even when the component is unmounted, resulting in a memory leak.  

## The Solution
The `bugSolution.js` file provides a corrected version.  A cleanup function is used to clear the interval when the component unmounts, preventing the memory leak.  This ensures that resources are properly released and prevents unexpected behavior.