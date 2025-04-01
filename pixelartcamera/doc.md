# Video Capture library

This library allows your app to access the camera (with user's consent)
and stream the result into a microStudio Image.

## Start the capture

You start the capture with a call to `startVideoCapture`:

```
  capture = startVideoCapture( width, height, view )
```

### Arguments

|argument|description|
|-|-|
|width|the width in pixels of the video|
|height|the height in pixels of the video|
|view|one of `"user"` (user facing camera) or `"environment"`|

### Return value

The function call returns a `capture` object.

### Example
```
  capture = startVideoCapture( 1280, 720, "user" )
```

## Use the capture

The `capture` object includes a set of properties and functions:

|field|description|
|-|-|
|`capture.image`|the captured image, which you can e.g. draw on screen|
|`capture.update()`|**this function must be called** everytime you want to refresh the camera view|
|`capture.status`|gives the status of the current capture|
|`capture.error`|gives error details, in case the status is "error"|
|`capture.stop()`|you can call this function to stop the media streaming|

