#2 Change Package Name

ex.  old > org.linphone
new > com.aaa.linphone

modify with git
'''
To create an apk with a different package name
You need to edit the build.gradle file:

look for the function named "getPackageName()" and change it value accordingly
also update the values in the AndroidManifest file where the comment appears
change the package name also in the files: res/xml/syncadapter.xml, res/xml/contacts.xml and res/values/non_localizable_custom where appears
run again the Makefile script by calling "make"
'''

open project with android studio
- new package name ex com.aaa
- move linphone to new folder
- select move all folder
- replace all old package name to new package name
