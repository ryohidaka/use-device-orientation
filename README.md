# use-device-orientation-hooks

[![npm version](https://badge.fury.io/js/use-device-orientation-hooks.svg)](https://badge.fury.io/js/use-device-orientation-hooks)
![build](https://github.com/ryohidaka/use-device-orientation-hooks/workflows/Build/badge.svg)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/B0B6TVH92)

## Overview

A React hook to obtain device orientation using DeviceOrientationEvent.

## Notes

## Installation

You can install this library using npm:

```shell
npm install use-device-orientation-hooks
```

## Usage

```tsx
import { useDeviceOrientation } from "use-device-orientation-hooks";

function App() {
  const [deviceOrientation, toggle] = useDeviceOrientation();

  return (
    <div>
      <p>Absolute: {deviceOrientation.absolute}</p>
      <p>Alpha: {deviceOrientation.alpha}</p>
      <p>Beta: {deviceOrientation.beta}</p>
      <p>Gamma: {deviceOrientation.gamma}</p>
      <p>Webkit Compass Heading: {deviceOrientation.webkitCompassHeading}</p>
      <p>Webkit Compass Accuracy: {deviceOrientation.webkitCompassAccuracy}</p>

      <button onClick={toggle}>Toggle Orientation Detection</button>
    </div>
  );
}
```

## API

### `useDeviceOrientation()`

A React hook that returns an array with two elements:

1. `deviceOrientation`: An object that represents the current device orientation. It has the following properties:

| Property                | Type           | Description                                                                                                       |
| ----------------------- | -------------- | ----------------------------------------------------------------------------------------------------------------- |
| `absolute`              | Boolean        | Indicates whether the device is providing absolute orientation data.                                              |
| `alpha`                 | Number         | The rotation of the device around the Z axis, representing a clockwise angle in degrees.                          |
| `beta`                  | Number         | The rotation of the device around the X axis, representing a forward or backward motion of the device in degrees. |
| `gamma`                 | Number         | The rotation of the device around the Y axis, representing a left or right motion of the device in degrees.       |
| `webkitCompassHeading`  | Number \| null | The direction that the device is facing according to the compass, in degrees.                                     |
| `webkitCompassAccuracy` | Number \| null | The accuracy of the compass heading in degrees.                                                                   |

2. `toggle()`: A function that can be used to start or stop the device orientation detection.

## Link

- [Window: deviceorientation event](https://developer.mozilla.org/en-US/docs/Web/API/Window/deviceorientation_event)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
