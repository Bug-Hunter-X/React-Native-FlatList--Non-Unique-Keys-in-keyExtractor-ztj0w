# React Native FlatList: Non-Unique Keys in keyExtractor

This repository demonstrates a common error in React Native's FlatList component: using a `keyExtractor` function that does not return unique keys for each item in the data array. This can lead to unexpected rendering behavior and performance issues.

## Bug Description
The `keyExtractor` function in the `bug.js` file uses the `id` property, but the `id` value 1 is repeated. This violates the uniqueness requirement of `keyExtractor`, resulting in incorrect rendering and potential performance problems.

## Solution
The `bugSolution.js` file demonstrates the solution: ensuring that each item in the data array has a unique key. In this case, we generate a UUID for each item to guarantee uniqueness.