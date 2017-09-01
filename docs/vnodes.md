# Virtual Nodes

A virtual node is a JavaScript object that represents a DOM tree.

```js
{
  tag: "div",
  data: {
    id: "app"
  },
  children: [{
    tag: "h1",
    data: null,
    children: ["Hi."]
  }]
}
```

To create a virtual node use the `h` function.

```js
const node = h("div", { id: "app" }, [
  h("h1", null, "Hi.")
])
```

Or [JSX](/docs/jsx.md), [hyperx](/docs/hyperx.md), [t7](https://github.com/trueadm/t7), etc., if you are already using a module bundler like [rollup](https://github.com/rollup/rollup) or [webpack](https://github.com/webpack/webpack).

```jsx
const node = (
  <div id="app">
    <h1>Hi.</h1>
  </div>
)
```

The VDOM engine consumes a virtual node to produce a DOM tree.

## Attributes

A virtual node attributes can be any valid [HTMLAttributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes), [SVGAttributes](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute), [DOMEvents](https://developer.mozilla.org/en-US/docs/Web/Events), [VDOMEvents](/docs/vdom-events.md) or [keys](/docs/keys.md).

