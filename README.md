# React useEffect Runs on Every Render Despite Dependency Array

This repository demonstrates a common issue in React where a `useEffect` hook runs on every render, even when a dependency array is provided. This often leads to unexpected behavior and performance problems.

## Bug Description

The provided `useEffect` hook intends to log a message only when the `count` state variable is greater than 0. However, due to an incorrect understanding of how `useEffect` works with dependency arrays, the effect runs on every render, resulting in multiple log messages and potential performance degradation.

## Solution

The solution involves using a better state management practice. In this case, we should only update state when the count changes from zero to a value greater than zero. In addition, it is recommended to add a condition to only log when count is updated successfully.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console logs as you increment the counter.  You'll notice that the log message appears on every render. This was caused by a missing condition in the useEffect hook.

## License

MIT