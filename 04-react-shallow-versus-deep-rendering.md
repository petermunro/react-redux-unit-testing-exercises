# Understanding Shallow versus Deep Rendering

1. Create a test to render two nested React components
   (such as your `<Contact />` component) using
   _shallow_ rendering. Use `myWrapper.debug()` to show the
   rendered output.

2. Create a new test to render the same components using
   _full_ rendering. Again show the rendered output with
   `myWrapper.debug()`.

3. Compare the two. How do they differ?

## Shallow Rendering and Refactoring

1. If you refactor your components so that the _parent_
   component renders the child's elements, does the
   test still pass?
