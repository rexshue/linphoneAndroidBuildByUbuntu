## Change Package Name

ex.    
old > org.linphone    
new > com.aaa.linphone

***modify with git***    
[git link](https://github.com/BelledonneCommunications/linphone-android/#to-create-an-apk-with-a-different-package-name)
```
To create an apk with a different package name
You need to edit the build.gradle file:

- look for the function named "getPackageName()" and change it value accordingly
- also update the values in the AndroidManifest file where the comment appears
- change the package name also in the files: res/xml/syncadapter.xml, res/xml/contacts.xml and res/values/non_localizable_custom where appears
- run again the Makefile script by calling "make"
```
build.gradle    
res/xml/syncadapter.xml    
res/xml/contacts.xml    
res/values/non_localizable_custom    

***open project with android studio***   
- new package name ex com.aaa    
In Android Panel, Select java, MouseR > New > Package > Select OK > new package name > OK
- move linphone to new folder    
Use MouseL drag linphone folder from old to new place    
option select move everything
- replace all old package name to new package name    
(Replace in path)
