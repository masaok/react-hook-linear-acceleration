A React hook to access data from the [Linear Acceleration API](https://developer.mozilla.org/en-US/docs/Web/API/LinearAccelerationSensor).

## Installation

Using `npm`:

```sh
npm install --save react-hook-linear-acceleration
```

Using `yarn`:

```sh
yarn add react-hook-linear-acceleration
```

## Usage

```jsx
import React from "react";
import useLinearAcceleration from "react-hook-linear-acceleration";

const MyComponent = () => {
  const sensor = useLinearAcceleration();

  return !sensor.error ? (
    <ul>
      <li>X: {sensor.x}</li>
      <li>Y: {sensor.y}</li>
      <li>Z: {sensor.z}</li>
    </ul>
  ) : (
    <p>No linear acceleration, sorry.</p>
  );
};
```

## Notes

Access to data from the Linear Acceleration API needs user permission.

If permission to access Linear Acceleration was previously granted by the user, Linear Acceleration data will be available. If permission to access was not granted previously, the user will be prompted to give permission when the component mounts.

## Caveats

Linear Acceleration API is available only in secure contexts (only using HTTPS).

## Credits

Credit to [Bence A. Tóth](https://github.com/bence-toth) for his original hook code for [Geolocation](https://www.npmjs.com/package/react-hook-geolocation).

## License

LGPL-3.0
