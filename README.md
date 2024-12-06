# Infinite useEffect Loop in React

This repository demonstrates a common error in React applications: an infinite loop caused by an improperly used `useEffect` hook. The `useEffect` hook, when not used correctly, can lead to performance issues and unexpected behavior.

## Bug Description
The provided `MyComponent` uses `useEffect` to log the count variable to the console. However, the dependency array is empty, meaning it runs after every render. This isn't inherently a bug, but combined with the state update, it creates an infinite render loop. 

## Bug Solution
The solution correctly includes `count` in the dependency array, ensuring `useEffect` only runs when `count` changes.  This avoids the infinite render loop.
