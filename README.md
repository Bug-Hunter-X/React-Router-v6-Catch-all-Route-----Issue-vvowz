# React Router v6 Catch-all Route Issue

This repository demonstrates a common issue encountered when using the catch-all route (`*`) in React Router v6.  The catch-all route, intended to handle any unmatched routes, is failing to render when navigating to a non-existent path.  The provided solution addresses this problem and provides the expected behavior.

## Problem

The problem lies in the order of routes defined within the `Routes` component.  If a more specific route is defined after the catch-all route, the catch-all route will never be reached.

## Solution

The solution involves reordering the routes to ensure the catch-all route is defined *last*. This ensures React Router considers it only after all other routes have been checked.