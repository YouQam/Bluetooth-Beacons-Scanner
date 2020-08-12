# Bluetooth-Beacons-Scanner
This application scans for nearby bluetooth low energy beacons. It was built using ionic cross-platform framework.  The implementation has been tested on both android & iOS devices.

## App Demo

Android            |  iOS
:-------------------------:|:-------------------------:
|<p align="center"><img src="https://i.imgur.com/nBDRyxf.gif" height="500" alt="alt text" title="demo"></p> |  <p align="center"><img src="https://i.imgur.com/VJXU0xD.gif" height="500" alt="alt text" title="demo"></p>

## Installation and Usage
- Clone / download the repo
- Run `npm install`
- Build & deploy to <b>Android</b>
  - Prerequisites
      - Java JDK 8
      - Android Studio
  - Run the following CLI commands
    - `ionic build`
    - `ionic cordova platform add android`
    - `ionic cordova run android` #To run on an android studio emulator
    - `ionic cordova run android  --device` #To run on a device

- Build & deploy to <b>iOS</b>:
  - Prerequisites
    - macOS
    - Xcode, install it from the App Store
    - iOS Developer account, sign up on [developer.apple.com](https://developer.apple.com/), it's free
  - Run the following CLI command
    - `ionic cordova build ios --prod`

## Note
In the project, I'm using estimote beacon with `UUID` = `b9407f30-f5f8-466e-aff9-25556b57fe6d`. In case you are using another company's product, just modify the UUID in path `src/app/home/home.page.ts`

```
 uuid = <Beacon UUID>;
```


## Troubleshooting
If all goes well it will start scanning for nearby beacons after pressing play button, but if you run into:
```
Cannot read property 'locationManager' of undefined
```
This is due to instability of the iBeacon plugin. To overcome the issue, replace some files with the ones you have in the project, [see here](https://github.com/YouQam/ionic5ibeacon).

## Licence
MIT
