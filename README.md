# React Native useRef Hook Error: Cannot read properties of null (reading 'current')

This repository demonstrates a common error encountered when using the `useRef` hook in React Native function components.  The issue arises from attempting to access properties of a ref before it's been assigned a value (initially it's `null`).  This can lead to runtime errors if not handled correctly.

## Problem:

The provided example showcases a scenario where a ref is used to access a native component, but due to asynchronous operations or component unmounting/remounting, the ref might be `null` when a method is called.

## Solution:

The solution shows how to safely access the ref by checking for `null` before attempting to access its properties. Using optional chaining (`?.`) or a conditional statement elegantly avoids the error.