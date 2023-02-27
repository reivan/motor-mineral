# Why useRef for usePrevious?

I was doing a [React coding question] from BigFrontEnd.dev. And solved it using a closure:

```jsx
let mem: any = undefined;

export function usePrevious<T>(value: T): T | undefined {
  const prevValue = mem;
  mem = value;

  return prevValue;
}
```

The solution was accepted. But other people in comments all used `useRef`:

```jsx
export function usePrevious<T>(value: T): T | undefined {
  const previous = useRef<T>();
  const toReturn = previous.current;
  previous.current = value;
  return toReturn;
}

```

And even `useEffect`:

```jsx
export function usePrevious<T>(value: T): T | undefined {
  const previous = useRef<T | undefined>()

  useEffect(() => {
    previous.current = value;
  }, [value]);

  return previous.current;
}
```

My question is why? Why is `useRef` better than a plain JavaScript variable?

[React coding question]: https://bigfrontend.dev/react/usePrevious
