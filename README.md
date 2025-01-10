# Infinite Rendering in React Component

This repository demonstrates a common React bug: infinite rendering caused by a missing dependency array in the `useEffect` hook.

## Bug Description

The `MyComponent` renders infinitely because the `useEffect` hook doesn't have a dependency array. This means the effect runs after every render, causing `setCount` to be called repeatedly, which triggers a re-render, leading to an infinite loop.

## Solution

The solution is to add the `count` variable to the dependency array. This ensures that the effect only runs when the value of `count` changes.