# Unity VR Cardboard demo

Google Cardboard Plugin per Unity
https://github.com/googlevr/cardboard-xr-plugin
API https://developers.google.com/cardboard/reference/unity

richiesto Unity 2020 LTS con modulo Android o iOS

Package https://github.com/googlevr/cardboard-xr-plugin.git

## Project Settings
Resolution and Presentation:
- Set the Default Orientation to Landscape Left.
- Disable Optimized Frame Pacing.

Other Settings:
- Choose OpenGLES2, or OpenGLES3, or both in Graphics APIs.
- Select IL2CPP in Scripting Backend.
- Select desired architectures by choosing ARMv7, ARM64, or both in Target Architectures.
- Select Require in Internet Access.
- Specify your company domain under Package Name.

- Select *Custom Main Gradle Template*
- Add the following lines to the **dependencies** section  to Assets/Plugins/Android/mainTemplate.gradle
```
implementation 'com.android.support:appcompat-v7:28.0.0'
implementation 'com.android.support:support-v4:28.0.0'
implementation 'com.google.android.gms:play-services-vision:15.0.2'
implementation 'com.google.protobuf:protobuf-lite:3.0.0'
```

- Select *Custom Main Manifest*
- Add the following attribute to the application tag of Assets/Plugins/Android/AndroidManifest.xml
```
<application android:requestLegacyExternalStorage="true" >
    ...
</application>
``` 

Project Settings > XR Plug-in Management
- Select Cardboard XR Plugin
- 