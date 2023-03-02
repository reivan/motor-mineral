# Component Reuse via Debugger

Sometime ago I had a component with around 15 props:

```jsx
<Chart
  lskjdfl={slkdjfk}
  sjfd={wsfh}
  data={data}
  otherData={fsjdf}
  some={foo}
  onChange={this.props.crops.flops.blops.do.something}
  {...ksdf}
/>
```

- no typescript, so no way of knowing how to use the component without looking inside
- deeply nested with props coming from redux and other sources
- no documentation

How do you reuse such a component?

## Solution

Just `console.log` props (or put a `debugger;` line):

```jsx
render() {
  console.log(this.props);

  return ...
}
```

Open the page where the component is used and the props object in dev tools.

Now you have the object from which you can figure out the types of individual props.

