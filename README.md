# React Memory Leak in useEffect with setInterval

This repository demonstrates a common React bug involving memory leaks caused by the improper handling of `setInterval` within a `useEffect` hook.  The bug occurs because the interval ID isn't properly cleaned up when the component unmounts, which leads to the interval continuing to run indefinitely, consuming resources.  The solution demonstrates the correct way to handle cleanup and prevent this type of memory leak.

## Bug
The `bug.js` file contains the faulty code, demonstrating the memory leak.  When the component is unmounted, the `setInterval` continues to run, resulting in a memory leak. 

## Solution
The `bugSolution.js` file provides the corrected code, ensuring that the `setInterval` is properly cleared when the component unmounts.  This effectively prevents the memory leak.  The solution uses `useEffect` with cleanup functionality to manage the interval.