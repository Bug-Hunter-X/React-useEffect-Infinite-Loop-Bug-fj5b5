# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook causing an infinite loop. The component renders repeatedly, leading to excessive console logging and potential performance issues.  The solution shows how to correctly use the dependency array to control the effect's execution.

## Bug Description

The provided `MyComponent` uses `useEffect` without a dependency array. This means the effect runs after every render, triggering another render and creating an infinite loop. The console will show a continuous stream of log messages.  This is a performance anti-pattern and should be avoided.

## Solution

The solution demonstrates how to fix this by providing a dependency array to the `useEffect` hook.  By only including `count` in the dependency array, the effect now only runs when the `count` value changes.