# React Router Catch-All Route Bug

This repository demonstrates a common issue with React Router v6's `Routes` component when using a catch-all route (`/*`).  The catch-all route, intended to handle all unmatched paths, can incorrectly match even when a more specific route should apply, leading to unexpected navigation behavior. 

## Problem
The problem arises when a catch-all route (`/*`) is placed after more specific routes. React Router will match the catch-all route before checking for more specific route matches, causing the intended route to never match. 

## Solution
The solution is to place the catch-all route at the end of the `Routes` component. This ensures that more specific routes are checked first, resolving the matching conflict.