# Use Enzyme to Perform a DOM Render

## Getting Started with Enzyme

1. Create a test file to test the `<Counter />` component.

2. In the test file, add a test:

   - First, `mount()` the React component, which will return a _wrapper_.
   - Then call `.find()` on the wrapper to locate the component.
   - Finally, assert that the component has been rendered with the correct string.

## Simulating a `Click` Event

A common bug is that the user clicks a button and the UI doesn't update.
With Enzyme, your test can simulate a `click` event and check that the rendered output has changed accordingly.

1. `mount()` your component as before.
2. Using the wrapper, `find()` the button.
3. `simulate*()` a `click` event.

Now to check that the UI (rendered output) has been updated:

1. `find()` the rendered component that should have been updated.
2. Check that its contents are correct.
