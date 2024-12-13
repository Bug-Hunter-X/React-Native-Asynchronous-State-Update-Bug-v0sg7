# React Native Asynchronous State Update Bug

This repository demonstrates a common bug in React Native applications where asynchronous state updates are not correctly handled.  The bug occurs when attempting to access a state variable immediately after calling `setState`, before the state has actually been updated.  The solution shows how to correctly handle this using functional updates and the `useEffect` hook.

## Bug Description

The issue arises because `setState` is asynchronous.  Code that runs immediately after `setState` may read the *old* value of the state variable, causing unexpected behavior.

## Bug Reproduction

1. Clone this repository.
2. Run `npm install`.
3. Run `npx react-native run-android` (or the equivalent for iOS).
4. Observe the console log - it'll show the incorrect value.

## Solution

The solution uses the functional update form of `setState` to ensure that the state variable is updated correctly, and that the access to the variable occurs *after* it has been updated.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](https://choosealicense.com/licenses/mit/)