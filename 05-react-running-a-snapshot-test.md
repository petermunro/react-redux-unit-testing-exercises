# Running A Snapshot Test

Snapshot tests enable you to see whether an unexpected change in your UI has happened.

They have their advantages and disadvantages though.

## Setting Up a Snapshot Test

We will set up a snapshot test for a simple component, such as `<Counter />`.

1. Create a test file, such as `Counter.snapshot.test.js`.

2. Insert the followng code:

   ```javascript
   import React from "react";
   import renderer from "react-test-renderer";

   import { Counter } from "./App";

   describe("Counter", () => {
     test("snapshot renders", () => {
       const component = renderer.create(<Counter counter={1} />);
       let tree = component.toJSON();
       expect(tree).toMatchSnapshot();
     });
   });
   ```

3. Run the test.

## Updating Snapshot Artifacts

1. Make a deliberate change to the UI.

   > In this case, some tests will fail as their snapshot files are now out-of-date.

2. To re-generate snapshots foiling tests, run:

   ```
   jest --updateSnapshot
   ```

3. Re-run all tests and ensure that they pass.
