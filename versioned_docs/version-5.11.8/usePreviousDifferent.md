---
id: usePreviousDifferent
title: usePreviousDifferent
sidebar_label: usePreviousDifferent
---

## About

usePreviousDifferent returns the last different value of a variable

[//]: # "Main"

## Installation

    npm install --save rooks

## Importing the hook

```javascript
import { usePreviousDifferent } from "rooks";
```

## Usage

```jsx
function Demo() {
  const [value, setValue] = useState(0);
  const previousValue = usePreviousDifferent(value);

  return (
    <div>
      <div>
        <p>Counter: {value}</p>
        <p>Previous Counter: {previousValue}</p>
        <button onClick={() => setValue(value + 1)}>Next</button>
      </div>
    </div>
  );
}

render(<Demo />);
```

### Arguments

| Arguments    | Type | Description                                                    | Default value |
| ------------ | ---- | -------------------------------------------------------------- | ------------- |
| currentValue | T    | The variable whose previously different value is to be tracked | undefined     |

### Return

| Returned value | Type | Description                                                     |
| -------------- | ---- | --------------------------------------------------------------- |
| previousValue  | T    | returns the past value which was different from the current one |

---

## Codesandbox Examples

### Basic Usage

<iframe src="https://codesandbox.io/embed/usepreviousdifferent-cvnhh?fontsize=14&hidenavigation=1&theme=dark"
  style={{
    width: "100%",
    height: 500,
    border: 0,
    borderRadius: 4,
    overflow: "hidden"
  }} 
  title="usePreviousDifferent"
  allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
  sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
/>

## Join Bhargav's discord server

You can click on the floating discord icon at the bottom right of the screen and talk to us in our server.
