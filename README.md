# Cordova 3.x plugin for Secugen fingerprint scanners

This plugin is for Phonegap/Cordova 3.x.

I'm not distributing the FDxSDKProAndroid.jar and its supporting armeabi dir - you must add those yourself and un-comment the relevant code.

This branch uses the Java port of [SourceAFIS](https://sourceafis.angeloflogic.com/) to process fingerprints. It is buggy and is not supported.

[Kiwi-Cordova](https://github.com/chrisekelley/kiwi-cordova) is a Cordova project that implements this plugin.

# Installation

I have not yet uploaded this to NPM, so you must clone this project and install it using the following commands:

    plugman install --platform android --project /pathToCordovaApp/platforms/android --plugin /Users/user/source/SecugenPlugin  
    rm -rf ../../plugins/org.rti.kidsthrive.secugen
    cp -Rf cordova/plugins/org.rti.kidsthrive.secugen ../../plugins    

# Development

Code for updating the plugin in your Cordova project:

    cordova build  
    plugman uninstall --platform android --project /pathToCordovaApp/platforms/android --plugin org.rti.kidsthrive.secugen   
    plugman install --platform android --project /pathToCordovaApp/platforms/android --plugin /Users/user/source/SecugenPlugin  
    rm -rf ../../plugins/org.rti.kidsthrive.secugen
    cp -Rf cordova/plugins/org.rti.kidsthrive.secugen ../../plugins
    cordova run android
