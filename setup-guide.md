# QuickStart Guide
Getting started with HISPlayer Video Upload consists of implementing the following steps:

1. Import HISPlayer SDK 
   
2. HISPlayer Video Upload Window

3. Using the Stream URL

4. Video Guide

## 1. Import HISPlayerSDK

Make sure the HISPlayer SDK has been imported to your Unity project. 
Importing the package is the same as importing other normal packages in Unity. 
Select the package of HISPlayer SDK and import it.

**Assets > Import Package > Custom Package > HISPlayerSDK unity package**

<p align="center">
<img width="650" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/f395a2e9-f224-4187-963b-aabb4e73eae9">
</p>

<br>

## 2. HISPlayer Video Upload Window

At the upper side of the Unity screen, open the window **Tools > HISPlayer > Upload Video**

<p align="center">
<img width="650" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/66fad0d0-6ca1-4983-b018-d8fe60684bf4">
</p>

It will open the HISPlayer Video Upload configuration window.

<p align="center">
<img width="450" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/52f9d871-43cc-4bad-8053-81d14fa7aa09">
</p>

Choose the streaming protocol **HLS** or **DASH** by selecting it from the dropdown menu. 
* Supported platforms for HLS : Android, iOS, WebGL, Windows, macOS.
* Supported platforms for DASH : Android, WebGL, Windows.

<p align="center">
<img width="450" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/3b8d3189-afd0-43f3-a235-be36614336ad">
</p>

Click on the **Upload Video** button. It will open a window to select the video file that you wish to upload. 

<p align="center">
<img width="650" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/b976d6cd-b555-418f-abb2-7145ef43ebcc">
</p>

After selecting the video file, it will start uploading to the server. The video content will be transcoded and published automatically. 
The whole process will take some time, please wait until the **Upload successful** message appears. Progress bar will be added in the next release. 
You may check the status message in the **Status** field of the HISPlayer Upload Video Window, or in the Unity console.

After **Upload successful** message has appeared, you will find the generated stream URL in the **Generated Stream URL** field or in the Unity console. 

<p align="center">
<img width="450" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/f1ff9d92-6b98-4287-87dc-f12703bd2d29">
</p>

<p align="center">
<img width="650" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/e8fd9c67-15e3-415c-98be-d6b74174b9ed">
</p>

Click the **Copy** button to copy the URL to the clipboard. 

Below is the generated stream URL example : 

```
https://content.hisplayer.com/getmedia/master.m3u8?contentKey=5C5nAbSM&protocol=hls
```

## 3. Using the Stream URL

Before using the generated stream URL, make sure that HISPlayer SDK has been configured following your target platform. Please refer to the following documentation : 
* Android : https://hisplayer.github.io/UnityAndroid-SDK/#/setup-guide?id=_12-configure-unity-for-android
* iOS : https://hisplayer.github.io/UnityiOS-SDK/#/setup-guide?id=_12-configure-unity-for-ios
* WebGL : https://hisplayer.github.io/UnityWebGL-SDK/#/setup-guide?id=_12-configure-unity-for-webgl
* Windows : https://hisplayer.github.io/UnityWindows-SDK/#/setup-guide?id=_12-configure-unity-for-windows
* MacOS : https://hisplayer.github.io/UnityMacOS-SDK/#/setup-guide?id=_12-configure-unity-for-macos

If you use [**HISPlayer Sample**](https://downloads.hisplayer.com/Unity/AllPlatforms/HISPlayer_Sample.unitypackage), please make sure the sample has been set-up properly : 
* Open HISPlayerSample/Assets/Scenes/**HISPlayerSample.unity**
* Import TextMesh Pro Essential
* Input the license key through the Inspector Window. **StreamController** game object -> **HISPlayerSample** component -> **License Key**

To change the default video URL using the new generated URL, go to 
**StreamController** game object > Inspector Window > **HISPlayerSample** (Script) > **HISPlayer Attributes** > **MultiStreamProperties** > **Url** > Replace the value with the new generated URL that you have copied previously.

<p align="center">
<img width="100%" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/c83a0e4b-13bf-488d-8bb8-73fe52eafc08">
</p>

After pasting the new generated URL, you may run your project through the Unity Editor or build your project targeting your desired platform (Android/iOS/WebGL/Windows/macOS). 

<p align="center">
<img width="650" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/75241072-c720-4809-96a5-b697052a666e">
</p>

## 4. Video Guide

Please refer to the following video guide to set-up HISPlayer Video Upload

[![Watch the video](https://img.youtube.com/vi/OEbIV7PW39w/sddefault.jpg)](https://youtu.be/OEbIV7PW39w)
