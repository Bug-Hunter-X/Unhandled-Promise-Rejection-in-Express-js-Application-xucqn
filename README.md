# Unhandled Promise Rejection in Express.js

This repository demonstrates a common error in Express.js applications: unhandled promise rejections in asynchronous operations.  The `bug.js` file showcases an Express app with an asynchronous function that may throw an error.  Crucially, it lacks proper error handling, leading to a potential crash or silent failure.  The `bugSolution.js` file provides the corrected version with comprehensive error handling.

## Problem

Asynchronous operations within Express.js routes often involve promises.  If these promises reject (due to errors), and the rejection is not handled, the application might not behave as expected.  In the worst case, this can lead to a server crash without any informative error messages.

## Solution

Implementing robust error handling is crucial.  Always use `.catch()` to handle potential promise rejections.  Proper error handling ensures graceful degradation of the app, providing meaningful feedback to users or administrators.
