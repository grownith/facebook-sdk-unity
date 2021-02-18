# Game Workstore Facebook SDK for Unity NPM

Unity NPM version of Facebook SDK! This repository applies the same license terms of the original version. 

Original version: [facebook-sdk-for-unity](https://github.com/facebook/facebook-sdk-for-unity)

# Installation

- Add the Google Scope:
  
  ```json
  "scopedRegistries": [
    {
      "name": "Game Package Registry by Google",
      "url": "https://unityregistry-pa.googleapis.com",
      "scopes": [
        "com.google"
      ]
    }
  ]
  ```

- Add following dependency to `Packages/manifest.json` in your project;

  ```json
  {
    "dependencies": {
      "com.google.external-dependency-manager": "1.2.164",
      "com.gameworkstore.facebooksdkunity": "git://github.com/GameWorkstore/facebook-sdk-unity?path=Assets/Package"
    }
  }
  ```

> For the official plugin, check out the [original repository](https://github.com/facebook/facebook-sdk-for-unity)

# FAQ

## About Facebook Developer Page Settings
For Unity Android games, add on facebook settings your packageName (com.example.etc) and your activityClass from manifest.
Go to advanced settings and enable "Native or desktop app?" to true. Respond "Is App Secret embedded in the client?" to false.
Don't include your client secret if not necessary in the app.

Convert SHA1 from GooglePlay console keysigns to KeyHash using this site:
http://tomeko.net/online_tools/hex_to_base64.php

## About GooglePlay reject default manifest

Change on the generated manifest the application xml node line android:debuggable value:
```
<application android:theme="@a... android:debuggable="true">
```
to false, that is it:
```
<application android:theme="@a... android:debuggable="false">
```