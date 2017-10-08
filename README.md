<p align="center">
  <a href="https://github.com/krausefx/detect.location">detect.location</a> &bull;
  <b>watch.user</b>
</p>

-------

# `watch.user`

[![Twitter: @KrauseFx](https://img.shields.io/badge/contact-@KrauseFx-blue.svg?style=flat)](https://twitter.com/KrauseFx)
[![License](https://img.shields.io/badge/license-MIT-green.svg?style=flat)](https://github.com/KrauseFx/watch.user/blob/master/LICENSE)

<a href="TODO"><img src="screenshots/WatchUser.png" align="right" width=80 /></a>

## Disclaimer

`watch.user` is not intended to be used in production. It's a proof of concept to highlight a privacy loophole that can be abused by iOS apps. Apps shouldn't use this. The goal is to close this loophole and give its users better privacy controls for the iPhone camera access.

## What does `watch.user` demonstrate?

Camera access is something that users often grant early in an app's life, to upload an avatar or send a photo. Those apps can use that permission to track the user's face, take pictures, or live stream their front and back camera, all without the user's consent or knowledge.

iOS camera permissions allow you to:

- Access the raw stream from the front and back camera of an iOS device any time your app is running and in the foreground
- Parse facial features in real-time like the eyes, mouth, and the face frame, in conjunction with the built-in iOS 11 Vision framework
- Know what your user is doing right now and where the user is located based on image data
- Upload random frames of the video stream to your web service, and run a proper face recognition software, which enables you to
  - Find existing photos of the user on the internet
  - Create a 3d model of the user's face
- Estimate the mood of the user based on what you show in your app (e.g., items in a news feed in your app)
- Detect if the user is on their phone alone, or watching together with a second person
- With the recent innovation around faster internet connections, faster processors and more efficient video codecs, a user probably won't notice if you live stream their camera onto the internet (e.g. while they sit on the toilet)
- Record stunning video content from bathrooms around the world, using both the front and the back camera, while the user scrolls through your feed

## Proposal

There are several solutions to this issue. 

- Provide an API for temporary access to the camera
- Show an icon in the status bar that the camera is active, and force the status bar to be visible whenever an app accesses the camera
- Add an LED to the iPhone's camera (both sides) that can't be disabled by application code

TODO: insert Radar here

## About the demo

The demo will show you innocent, random text. This could also be a feed to scroll through, a book to read, or an in-app browser. The demo will show you how an app can take pictures of you while you use it, once you give it permission to access the camera.

While you may think that you never grant the camera permission to apps, you should check: Settings > Privacy > Camera to see what apps you've actually granted access to your camera. Do you remember granting camera access to that app?

Chances are, if you use a messaging service like Messenger, WhatsApp, or Telegram, you've probably already granted permission to access both your image library ([detect.location](https://github.com/KrauseFx/detect.location)), and your camera.

## License

This project is licensed under the terms of the MIT license. See the [LICENSE](LICENSE) file.

Special thanks to [Pawel Chmiel](https://github.com/PChmiel), who built the foundation this project is based on with [VisionFaceDetection](https://github.com/DroidsOnRoids/VisionFaceDetection)

Special thanks to [Soroush](https://twitter.com/khanlou) for the idea to build a demo app for this.
