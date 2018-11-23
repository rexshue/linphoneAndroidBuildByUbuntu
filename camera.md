## Camera in linphone Android

image  
R.drawable.camera_button

/linphone-android/src/android/org/linphone/call/CallActivity
```
refreshInCallActions()
    video.setimageResource(R.drawable.camera_button);

hit camera

onClick()
    if(id == R.id.video)
        ...
        get PERMISSIONS_ENABLED_CAMERA


onRequestPermissionsResult()
    case PERMISSIONS_REQUEST_CAMERA:
        acceptCallUpdate(....);

acceptCallUpdate()
    ...
    //accept Call Video process
    if(accept){
        params.enableVideo(true);
        LinphoneManager.getLc().enableVideoCapture(true);
        LinphoneManager.getLc().enableVideoDisplay(true);
    }
    LinphoneManager.getLc().acceptCallUpdate(call, params);

```
