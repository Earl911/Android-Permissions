# Android-Permissions
On Android versions 6 (Marshmallow) and later, permssions are no longer requested during app installation; instead, permission acceptance must be requested by your app when it runs. If you fail to request these permissions, your app will not have access to external storage, gps, contact lists, etc.

Upon invocation from your app, Permissions.java will read your app's Android Manifest.xml file's permissions, which are still needed for Android releases prior to Marshmallow, and will then ask the user to individually accept or deny each permission. If a user denies a permission, he or she is shown the reason why the permission is necessary and is again requested to accept the permission. A list of denied permissions are returned to your app for taking appropriate action.

Your app would invoke Permissions.java early in its life cycle by passing it a list of reasons why it needs the permissions. Upon completion, Permissions.java will return a list of denied permissions for your app to handle.

Android maintains a list of accepted and denied permissions within its Application Manager. These permission settings can be changed via Android's Settings-Application Manager screens.

Permissions.java can be placed in a library's aar file for use by all your developed apps.

An Android Studio project folder is included for your use and understanding; however, only the Permissions.java file is needed in your apps.
