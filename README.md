# Uncontrolled setInterval in React Component
This repository demonstrates a common bug in React components involving the improper use of `setInterval`.  The `setInterval` function, without proper cleanup, can lead to memory leaks and unexpected behavior in your application.

## Bug Description
The `MyComponent` component uses `setInterval` to update the count every second. However, it fails to provide a cleanup function in the `useEffect` hook. This means that even after the component unmounts, the interval continues to run. This leads to memory leaks and potential issues.

## Solution
The solution involves using the cleanup function provided by `useEffect` to clear the interval when the component unmounts. This ensures that the interval is stopped when it is no longer needed.