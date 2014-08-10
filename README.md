release-android-library
=======================

Remote script to create a maven compatible release of an android library (aar)

####adding to your library
```
apply plugin: 'com.android.library'

ext {
    PUBLISH_GROUP_ID = 'com.blundell'
    PUBLISH_ARTIFACT_ID = 'example-library-name'
    PUBLISH_VERSION = '1.0.0'
}

android {
    // configs, flavors etc
}

dependencies {
    // dependencies
}

// Copy the file locally and use
apply from: 'android-release-aar.gradle'
// or use the remote copy to keep update with latest changes
apply from: 'https://raw.github.com/blundell/release-android-library/master/android-release-aar.gradle'
```


####useage

`./gradlew clean build generateRelease`

####example output


```
 :engine:zipRelease
 :engine:generateRelease
 Release 1.0.0 can be found at /Users/Blundell/Developer/git_repo/ExampleAndroidLibrary/build/release/1.0.0/
 Release 1.0.0 zipped can be found /Users/Blundell/Developer/git_repo/ExampleAndroidLibrary/build/release-1.0.0.zip

 BUILD SUCCESSFUL
 
 Total time: 23.609 secs
```