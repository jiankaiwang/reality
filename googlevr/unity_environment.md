# Build a GoogleVR Environment in Unity



Google VR is divided into two sub-fields, cardboard and daydreams. Both the above fields can be built in Unity, the developer can bulid the VR apps on Unity and further run it on the android device (or export it as a apk installation file).



## Preparation



* Download the latest Unity editor and install it : https://store.unity.com/
  * Free for Personal Usage (For beginners, students and hobbyists)
* Install the editor extension for unity to develop android apps :


  * If using old version unity, you would have to download `UnitySetup-Android-Support-for-Editor-5.x.x.exe`  (5.x.x is the version number) and install it.
  * If using latest version unity (e.g. `2017.2.0f3`). you could install the extension on the beginning step of installation, or re-run the installation file. 
* Download the latest the Google VR kit for Unity : `GoogleVRForUnity.unitypackage`
  * Refer to https://github.com/googlevr/gvr-unity-sdk/releases
* Download QuickTimeInstaller
  * Refer to https://support.apple.com/kb/DL837?locale=zh_TW
* Download Java SDK : http://www.oracle.com/technetwork/java/javase/downloads/index.html
* Download Android SDK : Suggest to use `Android Studio` to download different verison sdks. (Especially you are also a android app developer.)
  * In android studio, click `Tools`,  `Android`, `SDK Manager`. 
  * Downloaded (Suggested) SDK : Android `4.4.2 (API 19)`, `5.0.1 (API 21)`, `5.1.1 (API 22)`, `6.0 (API 23)`, `7.0 (API 24)` SDK platform
  * Suggested Tool : Android SDK Platform-tools v.25.0.4, Android SDK Tools v.25.2.5



## Developing Environment



* In unity, set the android `SDK`, `JDK` and `NDK` by clicking `Edit`, `Preferences`, `External Tools`, `Android`.
  * e.g. SDK : `C:\Users\user\androidSDK` (the same sdk download path of android studio)
  * e.g. JDK : `C:\Program Files\Java\jdk1.8.0_144`



## Import Google VR SDK



* In unity, import Google VR SDK by clicking `Assets`, `Import Packages`,`Custom Package`, and choosing the `GoogleVRForUnity.unitypackage` downloaded before.



## Build Environment Configuration



* Switch developing platform by clicking `File`, `Build Settings`,  on`Platform` view, choose `Android`, and click `switch platform`.
* On the same configuration view, click `Player Settings` and edit the following attributes (optional) : 
  * basic information : `Company Name`, `Product Name`, `Default Icon`.
  * `Rendering` on `Other Settings` : click `Virtual Reality Supported`; in `Virtual Reality SDKs`, choose `Cardboard` or `Daydreams`.
  * `Identification` on `Other Settings` : edit `Package Name` (Notice that the `package name` must be changed. You can't use default name from imported google VR.), `Version` (It can be string type.), `Bundle Version Code` (It used for internal version control and must be greater than the previous one.), `Minimum API Level` (Notice that the minimum API Level for cardboard is 4.4, on the other hand, daydreams is 7.0.), `Target API Level`.



## Load and Preview the GVR demo scene



* In the `project` view, click `Assets`, `GoogleVR`, `Demos`, `Scenes` and load the `GVRDemo`.
* If you use `Daydreams` platform, you could connect `Controller Phone` (not `Headset Phone`) and start to simulate the app on it.
* In unity, there are three buttons, `PLAY`, `STOP` and `RESUME`, on the top of design view. You can have a VR  view while chicking the `PLAY` button. You can hold the key `Alt` and move the mouse to see the whole scene. If you using `Daydreams`, you can use `Controller Phone` instead of mouse.



## Build and Deploy the Scene



* Build and Run : Connect to the headset phone and click `File`, `Build & Run` to start building and runing on the device.
* Build and Compile : Click `File`, `Build & Settings`, `Build` and a `apk` file would be generated for further manual installation.