Implementation:

- SolidJS removes Virtual DOM. Removing vdom diffing might mean better performance.
- SolidJS components run only once. Only `onMount` and no `onUpdate`.

Looking from ReactJS:

- props destructuring is not allowed (for reactivity to work)
- createEffect ~= useEffect

## References

- [Is SolidJS the better ReactJS?](https://youtu.be/w14cgW9pVkg)
- https://www.solidjs.com
