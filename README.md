# Christmas Stream



## Introduction

This repository hosts the software, settings and media used to run the yearly Our Lady's Grove bake off stream. It is frequently updated to ensure that all software continues to work far into the future. Here you can find documentation relating to managing and setting up the stream.

## Table of Contents

- Downloading the package (TBD)
- [Software used](#software-used)
- [Hardware used](#hardware-used)
- [Using OBS Studio](#using-obs-studio)
    - [Set up settings and scenes](#set-up-settings-and-scenes)
    - [Sign into YouTube](#sign-into-youtube)
    - [Starting stream](#starting-stream)
    - [Navigating the interface](#navigating-the-interface)
- [Using VDO.Ninja](#using-vdoninja)
    - [Creating a room](#creating-a-room)
    - [Adding cameras to OBS](#adding-cameras-to-obs)
    - [Messaging camera operators using VDO.Ninja](#messaging-camera-operators-using-vdoninja)
- [Using YouTube Studio](#using-youtube-studio)
    - [Creating a new broadcast](#creating-a-new-broadcast)
    - [Ending stream](#ending-stream)
- [Frequently asked questions](#frequently-asked-questions)
    - [Advanced FAQ](#advanced-faq)
- [Troubleshooting](#troubleshooting)

## Software used

- OBS Studio
- VDO.Ninja
- YouTube Studio

## Hardware used

- PC
    - The software packaged in this repository is intended for use on a computer room PC. If using a computer room PC, ensure it has at least the following requirements:
        - Intel Core i7, AMD Ryzen 5 or equivalent CPU*
        - 4GB of Memory*
        - Windows 10 1809**
       
            *Can be checked by pressing `Ctrl+Shift+Esc` and clicking on the `Performance` tab. The CPU and Memory specs should be displayed on the right hand side of the window after clicking on the corresponding graphs
        
            **Can be checked by pressing `Windows Key+R` and typing `winver`, a Window should appear displaying the Windows version

    - A non-school laptop can also be used, make sure it has the same requirements as above, but also ensure that it has a stable internet connection. If the laptop has an Ethernet port, use it for optimal performance.

- Phones or iPads (Minimum of 3)
    - iPhone 7 or later
    - Equivalent Android phone
    - Safari or Chrome
    - Two devices act as cameras, one device acts as a microphone
        - External microphone support has been finicky on Android, only works reliably on Safari on iPhone.

## Using OBS Studio

OBS (Open Broadcasting Software) Studio is a piece of software that allows the streaming of audio and video to platforms such as YouTube, Twitch, TikTok, among others. In our case, we use YouTube, as it is the platform that most people are used to, and allows the stream to be unlisted as opposed to public. To launch OBS Studio, open `File Explorer`, go to the ~USB~ via the sidebar and go to `[placeholderPathToOBS]`, and double-click on `OBS64.exe`

### Set up settings and scenes

- Settings are handled in OBS via `Profiles`. To set up the correct profile, in the top left hand corner click on `Profile` then `Import`, then select the `streamProfile` folder in the USB.
- Scenes are handled in OBS via `Scene Collections`. To set up the correct profile, in the top left hand corner click on `Scene Collections` then `Import`, then select the `streamSceneCollection.json` file.

### Sign into YouTube

Click on `Settings`, then `Stream`. From the `Service` dropdown, select `YouTube - RTMPS`. Click on `Connect Account (recommended)` and follow the on screen instructions to sign in.
- This will cause a new chat window to pop up. Since we do not use the YouTube live chat, feel free to X out of it.

### Starting stream

- First, [set up a stream in YouTube Studio](#creating-a-new-broadcast). Once that is done, go back to OBS Studio and click on `Manage Broadcast`. Go to the `Select Existing Broadcast` tab and select the stream you set up in the previous step. Click `Select broadcast and start streaming`. Go back to YouTube Studio and click `Go Live`.

### Navigating the interface

The appearance of your stream is dictated by your scenes and sources. Think of scenes like PowerPoint slides and sources being the text, images and videos on your slide. The higher up sources are on the source list, the more items it will overlap on stream. Clicking on a scene in the scene list changes the visible scene.

The audio mixer shows you everything that can play audio in your current scene. This includes microphones and any audio being played on the computer. These audio sources can be made louder or quieter individually using the volume sliders.

## Using VDO.Ninja

[VDO.Ninja](https://vdo.ninja/) is a website that allows us to use phones and iPads as cameras and microphones that connect to OBS wirelessly. This allows us to be versatile with the camera hardware used, and does not rely on any additional software on either the cameras or PC. It works by providing a link to the camera and audio feed that can be inputted into OBS via browser source.

### Creating a room

On the PC that you will be running OBS from, go to [VDO.Ninja](https://vdo.ninja/) and click on `Create a Room`. Enter a room name and a strong password, since any device in this room may be able to see other devices. To add more devices, send the `Invite a guest` link to the devices you wish to use as cameras.

On the cameras, use Safari or Chrome for best compatibility. When joining the room, ensure you are using the rear camera and in cases where multiple microphones are present (for example, if you have a built in microphone as well as one plugged in the headphone jack) make sure you choose the correct one.

### Adding cameras to OBS

Once you have a cameras in your room, add them to OBS by clicking `copy solo view link`, then finding the corresponding camera source in the source list, right click and selecting `Properties`, then pasting the link into the `URL` field.

### Messaging camera operators using VDO.Ninja

VDO.Ninja can also be used to message camera operators. In the director view, click on the message icon at the bottom of the page. This opens a chat window that lets you send messages to all other devices in the room. Use this to notify the camera operator when they are about to switch to their camera, or when switching away from their camera.

## Using YouTube Studio

[YouTube Studio](https://studio.youtube.com) is where you manage how the stream is displayed on YouTube. There are several settings that must be set up prior to going live.

### Creating a new broadcast

YouTube treats live streams similar to how it treats normal videos. Prior to the stream, you must provide a title, thumbnail and privacy setting. Once you are signed into the YouTube account, click on `Create` in the top right hand corner, then `Go Live`. This will bring you to the live streaming dashboard.

***Important: You must enable live streaming on the channel at least 24 hours before you intend to stream. If it does not prompt you to do so after clicking `Go Live`, ignore this warning***

Once you have enabled live streaming, click on `Schedule Stream` in the top right hand corner. Here, you will provide a title and thumbnail. Make sure that `How do you want to go live?` is set to `Streaming software`. Once you are on the `Visibility` tab, make sure that your stream is set to `Unlisted`. This will ensure that the link will work for teachers, but the stream will not show up on your channel or in search results.

Once you are done setting your stream settings, you are now on the stream landing page. Ensure that the stream latency is set to `Low latency` for a balance between delay and image quality. You are now ready to go live, make sure to start the stream in OBS Studio as explained [here](#start-stream).

### Ending stream

Once the stream is over, end it officially by clicking the `End Stream` button in the top right hand corner, then going back to OBS Studio and clicking `Stop streaming`.

## Frequently asked questions

*Is there a video guide?*

Not one made specifically for the bake-off stream. This documentation is intended for longevity, and video guides quickly become out of date. If there are any questions or concerns please create an issue for it. You can find many helpful guides on how to use OBS Studio, VDO.Ninja and YouTube Studio on YouTube.

*How do I know if the computer is powerful enough?*

Most of the computers in the computer room should be able to handle the stream, however a good way of testing it is by starting a recording first, then seeing if it looks choppy when you play it back. If it does, consider using another computer.

Another culprit for poor performance could be any videos being played on stream. OBS Studio handles some video formats better than others, and if in doubt, convert all video files to WEBM using tools such as [this](https://cloudconvert.com/webm-converter).

*How much preparation time is needed to set up the stream?*

To be safe, come into school about an hour beforehand. There are many moving parts to this setup and you may need to account for things such as charging devices, slow internet, load times and explaining the plan of action to other helpers.

### Advanced FAQ

*Why use GitHub?*

All of the software in this repository is designed to be run portably, which is necessary thanks to restrictions set on the school computers. It is also much easier to host the media files here than store them somewhere in the school where there is a chance it could be deleted, and there is no way to ensure that OBS Studio gets updated without using Git. It also provides insurance that nothing will be irreversably deleted thanks to version control.

*Can I merge any changes to this repository?*

Absolutely! If you have found that different settings work better, or you wish to change the scene collection, feel free to submit a merge request so that it can be used for future streams. Alternatively, fork this repository and use that version for later streams. There is obviously no license to this repository, so go nuts. Within reason.

***Important: If merging the profile folder, ensure that you have disconnected your YouTube account first, since this is a public repository and anyone can see revealing account information (source: the OBS Discord server)***

*Can this stream be handled remotely?*

Yes. It presents its own challenges, but given that VDO.Ninja does not require you to be on the same network as the cameras, OBS can technically be run from anywhere. Not recommended though.

## Troubleshooting

If you are encountering issues with any of the processes used to stream, create an issue for it. Be sure to use the appropriate label for your issue. Google is also your friend, there are many guides for using all the software used in this repo on YouTube, there are very few unique aspects to the files hosted here. Please also create an issue if you would like clarification on any step of this documentation, as it helps to improve it for the years to come. It is also encouraged to test out this configuration on a computer beforehand, to make sure everything is still working. Like mentioned before, a good way of doing this is by making a recording or a private stream on YouTube.
