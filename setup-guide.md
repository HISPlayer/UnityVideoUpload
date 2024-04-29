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
<img width="450" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/041506fb-dc64-4bb0-9bf4-33512d6613d9">
</p>

### HISPlayer Dashboard
This will direct you to the main HISPlayer Dashboard webpage. If you have not created an account yet, please create a new account on the HISPlayer Dashboard webpage by registering your email address.

### Email
The email address of your account that you have registered on HISPlayer Dashboard webpage. Please input the email address in the **Email** field.
If invalid email address is inputted, it will throw an error.

### Password
The password of your account that you have registered on HISPlayer Dashboard webpage. Please input the password in the **Password** field.
If invalid password is inputted, it will throw an error.

### Video Title
The title of the video that you will upload. You may input any text.

### Streaming Protocol

Choose the streaming protocol **HLS** or **DASH** by selecting it from the dropdown menu. 
* Supported platforms for HLS : Android, iOS, WebGL, Windows, macOS.
* Supported platforms for DASH : Android, WebGL, Windows.

<p align="center">
<img width="450" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/8a3ca8c8-d1ed-479f-b48b-725edd284e95">
</p>

### Upload Video
Click on the **Upload Video** button. It will open a window to select the video file that you wish to upload. 

<p align="center">
<img width="650" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/b976d6cd-b555-418f-abb2-7145ef43ebcc">
</p>

After selecting the video file, it will start uploading to the server. The video content will be transcoded and published automatically. 
The whole process will take some time, please wait until the **Upload successful** message appears.
You may check the status message in the **Status** field of the HISPlayer Upload Video Window, or in the Unity console. 
The progress bar indicates the overall video uploading, transcoding and publishing progress percentage. 

### Get the Stream URL

After **Upload successful** message has appeared, you will find the generated stream URL in the **Generated Stream URL** field or in the Unity editor console. 

<p align="center">
<img width="450" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/495e2435-6e6e-405b-839c-95d7b698d647">
</p>

Click the **Copy** button to copy the URL to the clipboard. 

Below is the generated stream URL example : 

```
https://api.hisplayer.com/media/master.m3u8?contentKey=AMqO1qIq
```

## 3. Using the Stream URL

Before using the generated stream URL, make sure that HISPlayer SDK has been configured following your target platform. Please refer to the following documentation : 
* Android : https://hisplayer.github.io/UnityAndroid-SDK/#/setup-guide?id=_12-configure-unity-for-android
* iOS : https://hisplayer.github.io/UnityiOS-SDK/#/setup-guide?id=_12-configure-unity-for-ios
* WebGL : https://hisplayer.github.io/UnityWebGL-SDK/#/setup-guide?id=_12-configure-unity-for-webgl
* Windows : https://hisplayer.github.io/UnityWindows-SDK/#/setup-guide?id=_12-configure-unity-for-windows
* MacOS : https://hisplayer.github.io/UnityMacOS-SDK/#/setup-guide?id=_12-configure-unity-for-macos

If you use **HISPlayer Sample**, please make sure the sample has been set-up properly : 
* Open Assets/HISPlayerSample/Scenes/**HISPlayerSample.unity**
* Import TextMesh Pro Essential
* Input the license key through the Inspector Window. **HISPlayerController** game object -> **HISPlayerController** component -> **License Key**

To change the default video URL using the new generated URL, go to 
**HISPlayerController** game object > Inspector Window > **HISPlayerController** (Script) > **HISPlayer Attributes** > **MultiStreamProperties** > **Url** > Replace the value with the new generated URL that you have copied previously.

<p align="center">
<img width="100%" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/2c9187f0-5a59-4b3d-8379-98ef070a3a1a">
</p>

After pasting the new generated URL, you may run your project through the Unity Editor or build your project targeting your desired platform (Android/iOS/WebGL/Windows/macOS). 

For more details about using HISPlayer Sample, please refer to the following documentation [**HISPlayer Sample**](https://hisplayer.github.io/UnitySamples/#/hisplayer-sample)

## 4. Video Guide

Please refer to the following video guide to use HISPlayer Video Upload

[![Watch the video](https://img.youtube.com/vi/RmnpeqIrYuM/sddefault.jpg)](https://youtu.be/RmnpeqIrYuM)
