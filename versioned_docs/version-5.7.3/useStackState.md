---
id: useStackState
title: useStackState
sidebar_label: useStackState
---

## About

A React hook that manages state in the form of a stack

[//]: # "Main"

## Installation

    npm install --save rooks

## Importing the hook

```javascript
import { useStackState } from "rooks";
```

## Usage

```jsx
function Demo() {
  // here list is still 1,2,3
  // listInReverse is basically list in stack order.
  // which is last-in first-out
  // so basically listInReverse = 3,2,1
  // controls contains utils to change the stack;
  const [list, controls, listInReverse] = useStackState([1, 2, 3]);
  const { push, peek, pop, length } = controls;

  // push(1)
  // pop()
  // peek()

  // This will render items in LIFO order
  return (
    <div>
      {list.map((item) => (
        <span>{item}</span>
      ))}
    </div>
  );
}

render(<Demo />);
```

### Arguments

| Arguments   | Type  | Description | Default value |
|-------------|-------|-------------|---------------|
| initialList | any[] | An array    | undefind      |

### Returned array items

| Returned items | Type     | Description                             |
|----------------|----------|-----------------------------------------|
| push           | function | Put an item to the top of the stack     |
| pop            | function | Remove the item on the top of the stack |
| peek           | function | Return the item on the top of the stack |
| length         | number   | Number of items in the stack            |

---

## Codesandbox Examples

### Basic Usage

<iframe 
  src="https://codesandbox.io/embed/bold-smoke-iedi8?fontsize=14&hidenavigation=1&module=%2Fsrc%2FApp.js&theme=dark"
  style={{
    width: "100%",
    height: 500,
    border: 0,
    borderRadius: 4,
    overflow: "hidden"
  }}
  title="useStackState"
  allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
  sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts" 
/>

## Join Bhargav's discord server

You can click on the floating discord icon at the bottom right of the screen and talk to us in our server.
