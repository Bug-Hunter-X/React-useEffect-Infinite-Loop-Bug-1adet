# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications involving the `useEffect` hook.  The example shows an infinite loop caused by a missing dependency array in `useEffect`.

## Description
The `useEffect` hook is used to perform side effects after a component renders.  However, if the dependency array is omitted or incorrectly specified, the effect will run after every render, potentially causing infinite loops or unexpected behavior.

## How to Reproduce
Clone the repository and run `npm install` to install the dependencies.  Then, run `npm start`. Observe the console output.  You will see that the message 'Count: ...' appears repeatedly, filling the console with log messages because the component re-renders constantly.

## Solution
The solution involves correctly specifying the dependency array in the `useEffect` hook. By adding `[count]` as the dependency array, the effect only runs when the `count` state variable changes. This fixes the infinite loop.
