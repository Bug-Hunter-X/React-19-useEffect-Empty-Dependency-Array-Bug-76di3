# React 19 useEffect Empty Dependency Array Bug

This repository demonstrates a subtle bug related to the `useEffect` hook in React 19 when used with an empty dependency array.  The provided code intends to log a message whenever the `count` state variable exceeds 0. However, due to the empty dependency array `[]`, the effect only runs once on the initial mount and never again, even when the count changes.

## Bug Description:
The `useEffect` hook with `[]` as the dependency array is intended to run only once on mount.  However, it is common for developers to make unintended logic errors in the effect, such as the one shown in this example, resulting in unexpected behavior.

## Solution:
The correct way to handle updates to the `count` variable is to include `count` in the dependency array.  This ensures the effect runs whenever `count` changes.