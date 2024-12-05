# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug causes an infinite rendering loop, leading to performance issues and potential crashes.

## Bug Description

A `useEffect` hook without a dependency array will execute after every render. In the provided example, the `useEffect` hook logs the current `count` value. Because `setCount` is called within the component which triggers a re-render, this hook runs infinitely, leading to a loop. 

## Solution

The solution involves adding a dependency array to the `useEffect` hook. This array specifies which values the hook should watch for changes. Only when one of these values changes will the effect run again.