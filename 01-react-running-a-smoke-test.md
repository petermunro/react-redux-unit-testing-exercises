# Running a Smoke Test

A Smoke Test enables you to check that the test setup is working.
While a very simple test, it tells you that:

- the test runner (Jest) is configured correctly
- the test framework libraries (eg Enzyme or React Testing Library) have
  been loaded correctly
- React and/or other UI libraries have been loaded

## Add a Smoke Test

Once you have a simple app running (eg with `create-react-app`),
add a test file such as `src/App.smoke.test.js`.
What you put in it will depend on which libraries and tools you
want to test for.

Below are two examples. The first tests that our test runner works.
The second tests that Enzyme has been loaded and configured correctly.

### Example Basic Smoke Test

```javascript
describe("Basic Test Suite", () => {
  it("Simple Smoke Test", () => {
    expect(true).toEqual(true);
  });
});
```

### An Example Smoke Test for Enzyme

```javascript
import React from "react";
import { shallow } from "enzyme";
import App from "./App";

it("renders without crashing", () => {
  shallow(<App />);
});
```

## Running the Tests

In a terminal, run the `test` script from `package.json` using either `npm` or `yarn`:

```
npm run test
```

or

```
yarn test
```
