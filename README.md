# React useEffect: Missing Cleanup in setInterval

This repository demonstrates a common error in React applications involving the `useEffect` hook and the `setInterval` function.  The example showcases how forgetting to clear the interval in the cleanup function leads to a memory leak and can cause unexpected behavior.

## The Problem

The provided `MyComponent` uses `setInterval` to update a counter every second.  However, it omits the crucial cleanup function within the `useEffect` hook to stop the interval when the component unmounts. This results in the interval continuing indefinitely even after the component is removed from the DOM, consuming resources and potentially causing unexpected side effects.

## The Solution

The solution file corrects the issue by adding a cleanup function that uses `clearInterval` to properly stop the `setInterval` when the component is unmounted.