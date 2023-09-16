# demo-list

## Overview

This GitHub repository, named "demo-list," is a demonstration of a simple React application that showcases several key concepts in React development. The repository consists of three main components:

1. **App.js**: This is the entry point of the application. It uses React hooks and functional components to manage the state of a list's title and its items. The primary concepts demonstrated here include `useState`, `useCallback`, and `useMemo`. Additionally, it integrates two other components, `DemoList` and `Button`.

2. **DemoList.js**: This component is responsible for rendering a list of items. It also demonstrates the use of the `useMemo` hook to optimize performance by memoizing the sorted list of items. It further showcases how props are passed down to child components.

3. **Button.js**: This is a simple button component used in the `App` component. It demonstrates the use of `React.memo` to memoize functional components and prevent unnecessary re-renders.

## App.js

### Concepts Demonstrated:

- **useState**: Used to manage the state of the list's title.
- **useCallback**: Utilized to memoize the `changeTitleHandler` function to avoid unnecessary re-renders.
- **useMemo**: Memoizes the `listItems` array to optimize performance.

### Description:

- The `App` component is the main entry point of the application.
- It manages the state of the list's title using the `useState` hook.
- `changeTitleHandler` is a memoized function that changes the list's title to "New Title" when the "Change List Title" button is clicked.
- `listItems` is memoized using `useMemo` to prevent unnecessary calculations.
- It renders the `DemoList` component, passing the title and items as props, and a `Button` component to change the list's title.

## DemoList.js

### Concepts Demonstrated:

- **useMemo**: Memoizes the sorted list to optimize performance.
- **Props**: Receives and uses props to render the list.

### Description:

- The `DemoList` component is responsible for rendering a sorted list.
- It uses the `useMemo` hook to memoize the sorted list of items, optimizing performance.
- The sorted list is rendered inside an unordered list (`ul`).
- The `props` object is destructured to access the `items` and `title` passed down from the parent component.

## Button.js

### Concepts Demonstrated:

- **React.memo**: Memoizes the `Button` component to prevent unnecessary re-renders.
- **Props**: Utilizes props for configuration.

### Description:

- The `Button` component is a simple button element with some styling.
- It uses `React.memo` to memoize the component, ensuring it only re-renders when its props change.
- Various button attributes, such as `type`, `className`, `onClick`, and `disabled`, are configured using props.
- The `children` prop is used to render the button's label.

These three components work together to create a basic React application that demonstrates the use of hooks, memoization, and prop handling. It can serve as a starting point for learning React concepts or as a reference for implementing similar functionality in your own projects.
