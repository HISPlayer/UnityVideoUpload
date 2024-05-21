# QuickStart Guide
Getting started with HISPlayer Video Upload consists of implementing the following steps:

1. Import HISPlayer SDK 
   
2. HISPlayer Video Upload Window

3. Use the Stream URL

## 1. Import HISPlayerSDK

Video Upload feature is supported from **HISPlayer SDK v4.0.0 and above**.
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
This button will direct you to the main HISPlayer Dashboard webpage, or you can open https://dashboard.hisplayer.com/ with your browser. If you have not created an account yet, please create a new account on the HISPlayer Dashboard webpage by clicking **Sign up**. It is mandatory to create an account before using HISPlayer Video Upload feature.

Please register your name, email address and password. After signing up, you will need to confirm for the email address verification.

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

## 3. Use the Stream URL

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

## HISPlayer Dashboard

You can verify the videos that have been uploaded on HISPlayer Dashboard. Please open https://dashboard.hisplayer.com/ with your browser, or you can click on **HISPlayer Dashboard** button on the [HISPlayer Video Upload Window](https://hisplayer.github.io/UnityVideoUpload/#/setup-guide?id=_2-hisplayer-video-upload-window). 

Input your email and password and click **Sign in**.

<p align="center">
<img width="100%" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/d0b5f7a7-fafc-4be0-aca4-4aa992070df1">
</p>

After sign in, you can check all the videos that have been uploaded. You can click on the video **ID** to check the generated HLS and DASH URLs and the video stream preview.

<p align="center">
<img width="100%" src="https://github.com/HISPlayer/UnityVideoUpload/assets/32887298/8ec09f7c-c318-42bc-882c-9c7fdca7ccb0">
</p>


## Video Guide

Please refer to the following video guide to use HISPlayer Video Upload

[![Watch the video](https://img.youtube.com/vi/RcpR1Yx1DzA/sddefault.jpg)](https://youtu.be/RcpR1Yx1DzA)
