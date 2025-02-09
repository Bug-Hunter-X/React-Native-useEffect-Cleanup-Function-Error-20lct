# React Native useEffect Cleanup Function Error

This repository demonstrates a common error in React Native applications involving the `useEffect` hook and its cleanup function.  The problem arises when the cleanup function attempts to interact with component state or props after the component has unmounted, leading to errors.  The solution involves checking if the component is still mounted before performing any actions within the cleanup function.

## Problem
The `bug.js` file shows the problematic code.  The `useEffect` hook sets an interval, and the cleanup function tries to clear the interval. However, if the component unmounts before the cleanup function runs, this can throw an error.

## Solution
The `bugSolution.js` file demonstrates the corrected code. It introduces a `mounted` state variable to ensure that actions within the cleanup function are only performed if the component is still mounted.