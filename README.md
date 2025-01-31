# React Native: Uninitialized State Access in Functional Component

This repository demonstrates a common error in React Native functional components: accessing state variables before they've been initialized. This often manifests as unexpected behavior or runtime errors.

## Problem

The `bug.js` file shows an example of a functional component where the `count` state variable is accessed within a `useEffect` hook without specifying a dependency array.  This results in the `count` value being `undefined` during the initial render, potentially causing errors.

## Solution

The `bugSolution.js` file presents the corrected version. By adding `count` to the dependency array of the `useEffect` hook, the effect only runs after the state variable has been initialized, thus avoiding the uninitialized access error.