# Unnecessary Re-renders in useEffect Hook

This example demonstrates an issue with unnecessary re-renders in a React component caused by an incorrectly used `useEffect` hook.  The `useEffect` hook, without the correct dependency array, causes an infinite loop and unnecessary console logging.

## Bug
The provided code shows an infinite loop which causes the component to re-render infinitely. This is caused by logging count changes within the useEffect hook without specifying the dependency array correctly. The useEffect function is called after every render, which keeps changing the count infinitely. 

## Solution
The solution involves correctly specifying the dependency array in the `useEffect` hook. By adding `[count]` as the dependency array, the effect only runs when the `count` value changes, fixing the infinite loop.