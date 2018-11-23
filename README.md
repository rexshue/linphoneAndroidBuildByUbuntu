Linphone Android Build By Ubuntu 18.04
----
Ubuntu 18.04 (64 Bit)
Linphone Android
JDK 8u
Android Studio
(NDK)
----
Step 1 Install JDK8 (Oracle)

    sudo add-apt-repository ppa:webupd8team/java
    sudo apt-get update
    
    sudo apt-get install oracle-java8-installer
    
    sudo update-alternatives --config java
    
    java -version

----
Step 2 Download Android Studio

goto https://developer.android.com/studio/

/etc/profile
    export ANDROID_HOME=/root/Android/Sdk
    export ANDROID_NDK=/root/Android/Sdk/ndk-bundle
    export PATH=$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools:$ANDROID_NDK:$PATH
    export GRADLE_HOME=/home/user/android-studio/gradle/gradle-4.6
    export PATH=$GRADLE_HOME/bin:$PATH

----
Step 3 Get Linphone Android source code

    git clone git://git.linphone.org/linphone-android.git --recursive
    
    sudo apt-get install yasm nasm ant intltool cmake vim-common lib32ncurses5 lib32z1 pkg-config
    
    sudo apt install python-pip
    pip install pystache
    
    sudo apt install libudev-dev doxygen graphviz

./prepare.py

make


