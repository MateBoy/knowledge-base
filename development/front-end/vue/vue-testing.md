`vue-test-utils` is the official unit testing library for Vue.js.

## Wrapper

A `Wrapper` is an object containing the mounted component or vnode and methods to test these.

### Properties

#### vm
This is the `Vue` instance.

#### element
The root DOM node of the wrapper

#### options
`options.attachedToDocument`
Returns true if component is attached to document when rendered.

### Methods

#### HTML
Returns HTML of `Wrapper` DOM node as a string.
```
wrapper.html()
```

## Common Issues
Here are some common issues you might run into when unit testing Vue.

### I trigger events on components but the DOM isn't updating
Cause: Vue re-renders the DOM asynchronously, so you need to wait for this update explicitly.
Before this could be done with a setting when mounting your Vue component in your tests via the `sync: true` flag, but this was depcreated on November 28th, 2019, as per the [changelog](https://github.com/vuejs/vue-test-utils/blob/dev/CHANGELOG.md#100-beta30-2019-11-28).

```javascript
it('render text', async () => {
    const wrapper = mount(TestComponent)
    
    wrapper.trigger('click')
    await Vue.nextTick()
    
    wrapper.text().toContain('some text')
    
    wrapper.trigger('click')
    await Vue.nextTick()
    wrapper.text().toContain('some different text')
})
```