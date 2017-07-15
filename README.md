# inman-vr

> Virtual Reality scene of Inman Square, Cambridge & Somerville, MA


## What?

The goal of this project is to build a virtual reality simulation of the intersection of Cambridge Street and Hampshire Street in Cambridge, MA.

## Who?

This project is being built at [Code for Boston](https://codeforboston.org).

The project lead is Matt Cloyd, the Chair of the Inman Square Neighborhood Association.

## Why?

At first, we had planned to build this project as a way to give Cambridge and Somerville residence a fuller, more experiential picture of the plans for Inman Square. Due to the rapid pace of this project in the City of Cambridge, however, we're not going to be able to fulfill our brilliant dreams of building a textured, animated, data-driven-traffic-simulation version of virtual Inman Square.

Instead, we're using this as a test simulation for early academic research into the effect of virtual reality on a public planning process. We're attempting to be only as detailed as the latest plans from the City of Cambridge, and we'll be comparing how 

## How? (Building on iOS)

Okay, ready to get into some gross technical details? Here goes.

Before starting, download:

- [Unity 5.4.5 from the Download Archive][unitydl]
- [Google VR SDK 1.20.0][vrsdk]. (I don't actually know if you'll need it, but.)
- [XCode][xcode]

[unitydl]: https://unity3d.com/get-unity/download/archive
[vrsdk]: https://github.com/googlevr/gvr-unity-sdk/raw/v1.20.0/GoogleVRForUnity.unitypackage
[xcode]: https://itunes.apple.com/us/app/xcode/id497799835?mt=12

> P.S. These instructions were written by a Rubyist web developer. I don't really know what I'm doing, but this is how I got it to work.

First, download the Unity project. The link is coming, but if you ping @matt on [Slack][slack], he'll send it to you. (What terrible documentation, I know. It's too big for GitHub, and it's going to take a bit to get it up on Dropbox or someplace else accessible. Sorry. You're so kind and patient.)

Next, go to File > Build Settings. Click "iOS" (or Android if that's your jam) and click "Switch Platform". If nothing happens, cool, then things are fine. If something starts happening, it's going to take kind of a while.

Make sure your iPhone is plugged in to a USB port.

Then, either from the File menu or the Build Settings window you left open, click "Build and Run". This should open up XCode.

You'll get errors. You'll need to sign your app (basically, verify your identity as a developer), and you'll need to fill in the project identifier with something related to whatever you set up to sign your bundle. (Ping me on [Slack][slack] again, sorry.)

While you're here, make sure you're building for iPhone only (change where it says Universal to iPhone), and also select the interface dropdown below that that contains the word "iPhone" and ends in ".xib". Also, uncheck all the allowed orientations except "Landscape Left", because that's the only orientation that Google Cardboard likes.

[slack]: https://cfb-public.slack.com

At this point, you should see an icon on your phone with the Unity logo and the name of the project. If XCode said something about not being able to run your app because it's untrusted, open your iPhone's Settings app. Go to General > Device Management (near the bottom) > the email address you associated with your Apple Developer account > the app name.

This will set the new developer app as trusted, so you can run it on your phone. Go back to the home screen, find the app, and run it. Tilt it left, and you should see two beautiful eyeballs-full of virtual Inman Square.
