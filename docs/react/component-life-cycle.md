## 📋 Understanding the Component Lifecycle in React (Using Functional Components)

### What is the Component Lifecycle?

In React, the component lifecycle refers to the series of events that happen from the creation of a component to its destruction. With the advent of hooks, functional components can now handle lifecycle events, making them more versatile and powerful.

### Lifecycle Methods in Functional Components

React hooks provide a way to handle component lifecycle events in functional components. The primary hooks used for lifecycle management are `useEffect`, `useLayoutEffect`, and `useRef`.

#### `useEffect` Hook

The `useEffect` hook allows you to perform side effects in your functional components. It serves a similar purpose to `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount` in class components.

##### Basic Usage

```jsx
import React, { useState, useEffect } from 'react';

function ExampleComponent() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    // Runs on mount and update
    document.title = `You clicked ${count} times`;

    // Cleanup function (runs on unmount)
    return () => {
      document.title = 'React App';
    };
  }, [count]); // Dependency array

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  );
}
```

### How `useEffect` Works

1. **Mounting and Updating**: By default, `useEffect` runs after every render. You can control this behavior by specifying dependencies.
2. **Cleanup**: The cleanup function within `useEffect` runs before the component unmounts and before subsequent effects.

### Example with Data Fetching

```jsx
import React, { useState, useEffect } from 'react';

function DataFetchingComponent() {
  const [data, setData] = useState([]);

  useEffect(() => {
    fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(data => setData(data));

    // Optional cleanup function
    return () => {
      // Clean up code (if any)
    };
  }, []); // Empty dependency array ensures this effect runs only once (on mount)

  return (
    <ul>
      {data.map(item => (
        <li key={item.id}>{item.name}</li>
      ))}
    </ul>
  );
}
```

#### `useLayoutEffect` Hook

The `useLayoutEffect` hook is similar to `useEffect`, but it runs synchronously after all DOM mutations. It is useful for reading layout from the DOM and synchronously re-rendering. It's a good choice for handling tasks that require the DOM to be in a certain state before proceeding.

##### Basic Usage

```jsx
import React, { useLayoutEffect, useRef } from 'react';

function LayoutEffectExample() {
  const inputRef = useRef(null);

  useLayoutEffect(() => {
    // Runs synchronously after DOM updates
    inputRef.current.focus();
  }, []);

  return <input ref={inputRef} />;
}
```

#### `useRef` Hook

The `useRef` hook returns a mutable ref object whose `.current` property is initialized to the passed argument (`initialValue`). This object persists for the lifetime of the component.

##### Basic Usage

```jsx
import React, { useRef } from 'react';

function RefExample() {
  const inputRef = useRef(null);

  const focusInput = () => {
    inputRef.current.focus();
  };

  return (
    <div>
      <input ref={inputRef} type="text" />
      <button onClick={focusInput}>Focus the input</button>
    </div>
  );
}
```

### Conclusion

Functional components in React leverage hooks like `useEffect`, `useLayoutEffect`, and `useRef` to manage the component lifecycle. By understanding and utilizing these hooks, you can handle side effects, layout changes, and direct DOM manipulation efficiently within your functional components. This approach aligns with modern React practices, promoting cleaner and more maintainable code.