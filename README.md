# Silent Promise Rejection in React Native Fetch

This repository demonstrates a common issue in React Native development: silent promise rejections during asynchronous operations, specifically using `fetch` to retrieve data.  The `DataList.js` file contains the buggy code; the solution is found in `DataListSolution.js`.

## Problem

The original `DataList` component attempts to fetch data using `fetch`. However, it lacks robust error handling. If the `fetch` call fails (e.g., network issue, server error), the promise rejects silently, leaving the user with no indication of the problem.  The app might appear frozen or show unexpected behavior.

## Solution

The improved `DataListSolution.js` addresses this by properly handling potential errors within the `try...catch` block.  The `finally` block ensures that the loading state is correctly updated regardless of success or failure, providing better feedback to the user.  Specific error messages are displayed to help diagnose problems.