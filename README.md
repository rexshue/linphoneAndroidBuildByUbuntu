Linphone Android Build By Ubuntu 18.04
----
- Ubuntu 18.04 (64 Bit)
- Linphone Android
- JDK 8u
- Android Studio
- (android-ndk-r18b)

*All use root account*
----
**Step 1 Install JDK8 (Oracle)**
*Must use JDK8*

  sudo add-apt-repository ppa:webupd8team/java
  sudo apt-get update

  sudo apt-get install oracle-java8-installer

  sudo update-alternatives --config java

  java -version

----
**Step 2 Download Android Studio**

goto https://developer.android.com/studio/
Download Android Studio and unzip it.
Download NDK from android studio
Set envirorment value

/etc/profile
  export ANDROID_HOME=/root/Android/Sdk

  export ANDROID_NDK=/root/Android/Sdk/ndk-bundle

  export PATH=$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools:$ANDROID_NDK:$PATH

  export GRADLE_HOME=/home/user/android-studio/gradle/gradle-4.6

  export PATH=$GRADLE_HOME/bin:$PATH

  echo $JAVA_HOME
  echo $ANDROID_HOME

  source /etc/profile.d/jdk.sh
  source /etc/profile

----
**Step 3 Get Linphone Android source code**

  git clone git://git.linphone.org/linphone-android.git --recursive

  sudo apt-get install yasm nasm ant intltool cmake vim-common lib32ncurses5 lib32z1 pkg-config

  dpkg --add-architecture i386
  aptitude update
  aptitude install libstdc++6:i386 libgcc1:i386 zlib1g:i386 libncurses5:i386

  sudo apt install python-pip
  pip install pystache

  sudo apt install libudev-dev doxygen graphviz

./prepare.py

  ReRun
./prepare.py -c

make
----
** Step 4 Get Debug APK **
when make complete , the apk is in the folder

bin/outputs/apk/debug
