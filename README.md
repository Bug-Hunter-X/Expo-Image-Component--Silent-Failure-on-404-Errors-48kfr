# Expo Image Component: Silent Failure on 404 Errors

This repository demonstrates a bug in the Expo `Image` component where it silently fails to load images that return a 404 error.  The component doesn't provide any clear indication of the error, making debugging difficult.

## Bug Description

When an image URL returns a 404 error, the `Image` component doesn't display an error message or a placeholder image.  Instead, it might display a broken image icon or nothing at all. This makes it hard to determine why an image isn't loading.

## Solution

The solution involves adding error handling to gracefully manage 404 errors. This can be done by using the `onError` prop of the `Image` component to display a placeholder image or an error message when an image fails to load.