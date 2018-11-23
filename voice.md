## Voice Call 

**Register**
/src/android/org/linphone/assistant/AssistantActivity.java
```
lc.addProxyConfig(...)
lc.addAuthInfo(...)
lc.setDefaultProxyConfig(...)
```

**Voice Call**
/src/android/org/linphone/ui/CallButton.java
```
onClick()
	LinphoneManager.getInstance().newOutgoingCall(mAddress);
```
/src/android/org/linphone/LinphoneManager.java
```
newOutgoingCall()
	CallManager.getInstance().inviteAddress(...)

```

/src/android/org/linphone/call/CallManager.java
```
inviteAddress()
	lc.inviteAddressWithParams(...)
```

