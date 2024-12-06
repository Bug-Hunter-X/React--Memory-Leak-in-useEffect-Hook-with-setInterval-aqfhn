# React useEffect Memory Leak

This repository demonstrates a common mistake in React's `useEffect` hook that can lead to memory leaks. The example uses `setInterval` without proper cleanup, causing the interval to persist even after the component unmounts.

## Problem
The `setInterval` function continues to run in the background even after the component has been unmounted. This leads to memory leaks, particularly if it accesses component state or other resources that are no longer available.

## Solution
The `useEffect` hook provides a return function for cleanup actions. By calling `clearInterval` in the cleanup function, we ensure that the interval is stopped when the component is unmounted, preventing the memory leak.

## Usage
1. Clone the repository.
2. Install dependencies using `npm install`.
3. Run the project using `npm start`.

