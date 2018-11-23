##Camera in linphone Android

image  
R.drawable.camera_button

/linphone-android/src/android/org/linphone/call/CallActivity
```
refreshInCallActions()
    video.setimageResource(R.drawable.camera_button);

hit camera

onRequestPermissionsResult()
    case PERMISSIONS_REQUEST_CAMERA:
        acceptCallUpdate(....);
```
