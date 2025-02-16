# React Router DOM Route Parameter Missing Crash

This repository demonstrates a bug in React Router DOM v6 where the application crashes when navigating to a route that expects a parameter but the parameter is missing.  The issue occurs when using the `useParams()` hook to access the route parameters without proper handling of missing parameters.  A solution is provided using a conditional statement to check if the parameter exists.

## Bug

The bug lies in how the User component handles the case where the ':id' parameter is absent from the URL.  When the user navigates directly to '/users', the `useParams()` hook returns an empty object instead of a helpful indication of a missing parameter which causes a crash.

## Solution

The solution addresses this problem by explicitly checking if the 'id' parameter exists before attempting to use it within the User component.  The application will now gracefully handle the missing parameter instead of crashing.