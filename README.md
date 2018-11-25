# Android Smart WebView
<img src="https://img.shields.io/badge/language-java-orange.svg" /> <img src="https://img.shields.io/badge/version-3.0-yellow.svg" /> [![MIT Licence](https://badges.frapsoft.com/os/mit/mit.svg?v=103)](https://opensource.org/licenses/mit-license.php)

This project is developed to help you create Hybrid Android applications with just webview. Hybrid app comes in between webview and native forms, with this project you can embed any existing webpage or setup an Offline HTML/CSS/Javascript based project.

Android Smart WebView gathers all necessary information needed to make any simple app as powerful as a native Android app. This project takes only required data from device to obtain information, including, GPS Location, File Manager, Camera for Processing Images, Custom Dialogues, Notifications and more with clean minimal design.

## Getting Started
These instructions will help you get your Smart WebView copy up and running on your local machine for development and testing purposes.

### Requirement
The project requires minimum Android API 19+ (4.4 KitKat) SDK to test [API 16+ in previous version]. You can use any IDE according to your comfort, I used Android Studio (latest version by the project publish time) for this.

### Test Run
Try rebuilding the project in your programming environment, once you are done fixing any error (incase if one comes up), you'll be ready to look into the project.

### Permissions
You can remove any of the following requests if you do not need them or you can disable any feature using easy setup variables. Currently, these permissions are must for default variables to work properly.
```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
<uses-permission android:name="android.permission.ACCESS_WIFI_STATE" />
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
<uses-permission android:name="android.permission.CAMERA"/>
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.VIBRATE" />
```
`INTERNET` permission is required if you are requesting a weburl or webpage.
`WRITE_EXTERNAL_STORAGE` is required for camera photo creation, if you have enabled `ASWP_FUPLOAD` and `ASWP_CAMUPLOAD` to upload image files.

### Easy Setup
Once your project is ready here are some static variables you can change as per your app requirements.

#### Permission variables
```java
static boolean ASWP_JSCRIPT     = true;     //enable JavaScript for webview
static boolean ASWP_FUPLOAD     = true;     //upload file from webview
static boolean ASWP_CAMUPLOAD   = true;     //enable upload from camera for photos
static boolean ASWP_ONLYCAM     = false;	//incase you want only camera files to upload
static boolean ASWP_MULFILE     = true;     //upload multiple files in webview
static boolean ASWP_LOCATION    = false;     //track GPS locations
static boolean ASWP_RATINGS     = true;     //show ratings dialog; auto configured, edit method get_rating() for customizations
static boolean ASWP_PBAR        = true;     //show progress bar in app
static boolean ASWP_ZOOM        = false;    //zoom control for webpages view
static boolean ASWP_SFORM       = false;    //save form cache and auto-fill information
static boolean ASWP_OFFLINE     = false;    //whether the loading webpages are offline or online
static boolean ASWP_EXTURL      = true;     //open external url with default browser instead of app webview
```

#### Configuration variables
Complete URL of your website, landing page or local file as `file:///android_res/dir/file.html`
```java
ASWV_URL      = "https://github.com/mgks";	//domain, or directory or locating to any root file
```

If file upload enabled, you can define its extention type, default is `*/*` for all file types;

Use `image/*` for image types; check file type references on web for custom file type
```java
ASWV_F_TYPE   = "*/*";
```

## Getting GPS Location
If `ASWP_LOCATION = true` then the app will start requesting GPS locations of the device on regular basis and all of the recorded data will be sent to the webpage in form of cookies, with updated live GPS locations.
```java
COOKIE "lat" for latitude
COOKIE "long" for longitude
```

## License
This project is licensed under the MIT License - see [LICENSE.md](LICENSE.md) file for details or read [MIT license](https://opensource.org/licenses/MIT).

## Donate
#### I'd appreciate even your tiniest contribution to my work, it keeps me motivated to keep this Open Source updated. If this project helped you or your business in any way and you feel like donating some change, you can Paypal me from the button below.

<a href="https://ko-fi.com/Z8Z4BPQ6" target="_blank" title="Buy me a Coffee"><img width="150" style="border:0px;width:150px;" src="https://az743702.vo.msecnd.net/cdn/kofi2.png?v=0" border="0" alt="Buy Me a Coffee at ko-fi.com" /></a>

## [Get Smart WebView Pro](https://github.com/mgks/SmartWebView-Pro)
Smart WebView Pro is a commercial app built for small and medium level businesses, easy to implement with any existing environment.
```
PRO FEATURES:
- Firebase Push Notifications
- Google AdMob
- Navigation Drawer
- Search Bar
- Action Menu
- Chrome Tab for External URLs
- And more
```
**To Get Your Smart WebView Pro's copy, drop an email to [getmgks@gmail.com]**

**For SWV Pro Updates, Demo and Documentation, follow [SmartWebView-Pro](https://github.com/mgks/SmartWebView-Pro) repo.**

## Acknowledgment
Rating method (Android-Rate) used in this app is developed by [hotchemi](https://github.com/hotchemi) and thanks to other programmers who contributed to this project.

Post in Github Repo issues section if you got any problem handling the project and if you want to contribute, you're most welcome to help me make a smarter project than what it is.
Just drop me a mail at: [getmgks@gmail.com](mailto:getmgks@gmail.com)

**This project on Infeeds - [Android Smart WebView open source to upload files, get GPS locations and more advanced features](https://infeeds.com/d/CODEmgks/25019/android-smart-webview-open-source-upload)**

**A personal note:** `You all must keep up with programming. It's sometimes difficult and sometimes easy but fun afterall, you can create your own world with programming and that's the beauty of it. So, all the best for your next creation.`

This project is initially developed by **[Ghazi Khan](https://mgks.infeeds.com)**.

[![Profile](https://forthebadge.com/images/badges/built-with-love.svg)](https://github.com/mgks)
![ga tracker](https://www.google-analytics.com/collect?v=1&a=257770996&t=pageview&dl=https%3A%2F%2Fgithub.com%2Fmgks%2FAndroid-SmartWebView&ul=en-us&de=UTF-8&cid=978224512.1377738459&tid=UA-129370045-1&z=887657232 "ga tracker")
