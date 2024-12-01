## 📋 React Router DOM

### What is React Router DOM?

React Router DOM is a library that enables dynamic routing in a web application. It allows developers to create single-page applications with navigation and route management. It handles the browser's URL and maps it to the corresponding React components.

### Key Components and Hooks

- **BrowserRouter**: A router implementation that uses the HTML5 history API (pushState, replaceState, and the popstate event) to keep your UI in sync with the URL.
- **Routes** and **Route**: Components used to define the mapping between the URL and the React components.
- **Link**: A component used to create navigational links.
- **useNavigate**: A hook that provides navigation functionality.
- **Navigate**: A component for programmatic navigation.

### Setting Up Routes in `main.jsx` or `index.js`

#### Basic Setup

1. **Install React Router DOM**:

    ```bash
    npm install react-router-dom
    ```

2. **Configure Routes in `main.jsx` or `index.js`**:

    ```jsx
    import React from 'react';
    import ReactDOM from 'react-dom/client';
    import { BrowserRouter, Routes, Route } from 'react-router-dom';
    import App from './App';
    import Home from './components/Home';
    import Login from './components/Login';

    const root = ReactDOM.createRoot(document.getElementById('root'));

    root.render(
      <BrowserRouter>
        <Routes>
          <Route path="/" element={<App />}>
            <Route path="home" element={<Home />} />
            <Route path="login" element={<Login />} />
          </Route>
        </Routes>
      </BrowserRouter>
    );
    ```

### Navigation in React Router

#### Using the `<Link>` Component

The `<Link>` component is used to create navigational links. It is similar to an HTML anchor tag (`<a>`), but it uses the history API to prevent page reloads and handle navigation more efficiently.

```jsx
import React from 'react';
import { Link } from 'react-router-dom';

function Navbar() {
  return (
    <nav>
      <ul>
        <li>
          <Link to="/home">Home</Link>
        </li>
        <li>
          <Link to="/login">Login</Link>
        </li>
      </ul>
    </nav>
  );
}

export default Navbar;
```

#### Using the `useNavigate` Hook

The `useNavigate` hook provides a way to navigate programmatically in a functional component.

```jsx
import React from 'react';
import { useNavigate } from 'react-router-dom';

function Login() {
  const navigate = useNavigate();

  const handleLogin = () => {
    // Perform login logic
    // On successful login
    navigate('/home');
  };

  return (
    <div>
      <h2>Login Page</h2>
      <button onClick={handleLogin}>Login</button>
    </div>
  );
}

export default Login;
```

#### Using the `<Navigate>` Component

The `<Navigate>` component is used to navigate programmatically in a JSX context.

```jsx
import React from 'react';
import { Navigate } from 'react-router-dom';

function Login() {
  const isAuthenticated = false; // Example authentication status

  if (isAuthenticated) {
    return <Navigate to="/home" />;
  }

  return (
    <div>
      <h2>Login Page</h2>
      {/* Login form or logic */}
    </div>
  );
}

export default Login;
```

### Example Project Structure

```
src/
|-- components/
|   |-- Home.jsx
|   |-- Login.jsx
|-- App.jsx
|-- index.js
|-- main.jsx
```

### Complete Example

**`App.jsx`**:

```jsx
import React from 'react';
import { Outlet } from 'react-router-dom';
import Navbar from './components/Navbar';

function App() {
  return (
    <div>
      <Navbar />
      <Outlet />
    </div>
  );
}

export default App;
```

**`Home.jsx`**:

```jsx
import React from 'react';

function Home() {
  return <h2>Home Page</h2>;
}

export default Home;
```

**`Login.jsx`**:

```jsx
import React from 'react';
import { useNavigate } from 'react-router-dom';

function Login() {
  const navigate = useNavigate();

  const handleLogin = () => {
    // Perform login logic
    navigate('/home');
  };

  return (
    <div>
      <h2>Login Page</h2>
      <button onClick={handleLogin}>Login</button>
    </div>
  );
}

export default Login;
```

**`Navbar.jsx`**:

```jsx
import React from 'react';
import { Link } from 'react-router-dom';

function Navbar() {
  return (
    <nav>
      <ul>
        <li>
          <Link to="/home">Home</Link>
        </li>
        <li>
          <Link to="/login">Login</Link>
        </li>
      </ul>
    </nav>
  );
}

export default Navbar;
```

### Conclusion

React Router DOM is a powerful library for handling routing in React applications. Using components like `BrowserRouter`, `Routes`, `Route`, and hooks like `useNavigate`, you can efficiently manage navigation and routing in your app. The `Link` component allows for declarative navigation, while `useNavigate` and `<Navigate>` provide flexible programmatic navigation options. By understanding these tools, you can create a seamless and dynamic user experience in your React applications.