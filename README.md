# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from an incorrect dependency array, leading to an infinite render loop.

## Bug Description

The `MyComponent` component uses the `useEffect` hook to log the current value of the `count` state variable. However, the `setCount` function is called within the `useEffect` hook itself, which is not included in the dependency array. This causes the effect to run repeatedly, triggering a continuous re-render cycle and creating an infinite loop.

## Solution

The solution involves correctly specifying the dependency array for the `useEffect` hook. By adding `setCount` to the dependency array, the effect is only triggered when the `setCount` function changes, preventing the infinite loop. 