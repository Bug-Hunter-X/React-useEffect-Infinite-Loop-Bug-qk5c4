# React useEffect Infinite Loop Bug
This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from an incorrect dependency array, leading to an infinite loop of re-renders.

The `bug.js` file contains the buggy code. The `bugSolution.js` file provides a corrected version.

## Bug Description
The `useEffect` hook is used to perform side effects after a component renders.  If a value used inside the effect is not included in the dependency array, the effect will run on every render, potentially causing an infinite loop.

## Solution
To fix this, ensure that all values accessed inside the effect are included in the dependency array.  In this case, adding `count` to the dependency array prevents the effect from running unnecessarily when the `count` state updates.