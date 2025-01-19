**React**

# React Functional Components

## How do I unmount the Functional Component in React?

- The actions that needs to performed at the time of component unmount can be written in return from useEffect.
- Basically useEffect returns the callback in which we can perform the actions that needs to be performed at time of component unmount like clearing of setInterval, etc. Eg -

```javascript
useEffect(() => {
  const timer = setInterval(() => {
    console.log("Hello");
  }, 1000);

  return () => {
    clearInterval(timer);
  };
}, []);
```

- The return callback from useEffect() hook is called when component unmounts in React Functional Component.
