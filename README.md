# React Router Dom v6 - Unexpected behavior on non-existent route

This repository demonstrates an uncommon bug in React Router Dom v6 where navigating to a route that does not exist results in the application rendering nothing without any errors in the console.

## Bug Description
The application uses React Router Dom v6 to handle navigation between different components. When a user attempts to navigate to a route that is not defined in the `Routes` component, the application does not display an error message or render a default component. Instead, the screen remains blank.

## Reproduction Steps
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to a non-existent route (e.g., `/nonexistent`).

You'll observe that the application renders nothing instead of a 404 page or fallback route.

## Solution
The solution involves adding a `Route` component with a wildcard path (`/*`) that serves as a fallback for non-existent routes. This component can render a 404 page or a default component.