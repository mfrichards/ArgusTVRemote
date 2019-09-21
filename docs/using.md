## Users Guide (work in progress)
### Watching Recordings on the Device

When you select "Watch" for a recording within Argus TV Remote, Argus TV Remote will launch the recording on your device, and the system will then ask you to select a player from those installed on the device that can play back that type of recording. To watch recordings on your device, you must have installed a video player that supports the file type of your recordings (typically either MPEG2 or MPEG4 ".ts" files), and is able to read from the network shares where your recordings are stored. I have had the most success with either Kodi (for Android), VLC, or the Archos video player.

### Casting Recordings to Kodi

When you select "Watch On..." for a recording within Argus TV Remote, it will search for Kodi instances on the network, and present a list of any found. For Kodi instances to be auto-discovered, you must enable "Zeroconf" within Kodi (see below). For devices that are not discovered automatically, you can add them manually with the IP address and port. Once you select a Kodi instance, Argus TV Remote will then start the recording on that device and open the built in remote control so you can control playback.

Argus TV Remote is able to auto-discover Kodi instances on the same network. In order for auto discovery to work, you must enable "Zeroconf" in the Kodi settings:

1. In Kodi, go to Settings > Services > General.
2. Select "Annouce services to other systems" under "Zeroconf".
3. If running Kodi under Windows, you must also install Apple's "Bonjour" software.

**Note:** If you choose not to enable Zeroconf in Kodi, you can still configure Kodi instances in Argus TV Remote. You will just need to manually enter the IP address and control port of your Kodi server.

In order for Argus TV Remote to communicate with Kodi, you must also enable "Control via HTTP" within Kodi:

1. In Kodi, go to Settings > Services > Control.
2. Enable "Allow remote control via HTTP" under "Web Server".
3. Note the userid and password (if set), as well as the port if not using Zeroconf. You will need these in Argus TV Remote to connect to Kodi.

**Note:** Do not enable SSL - Argus TV Remote does not support SSL when communicating with Kodi.

### Watching Live TV

To view live TV on the device you must have installed a video player that supports the video format of your TV channels (usually either MPEG2 or MPEG4) and playing RTSP streams. Again, I have had the most success using either Kodi or VLC as the player. When you select "Watch Live" from a guide channel in Argus TV Remote, it will start the Live stream, and then the system will then ask you to select a player from those installed on the device that support playing RTSP streams.

When you select "Watch Live On..." for a guide channel within Argus TV Remote, just like when casting recordings it will search for Kodi instances on the network and present a list of any found. Once you select a Kodi instance, Argus TV Remote will then start the live stream on that device and open the built in remote control so you can control playback.

Note: When watching live TV, it is important that you do not exit Argus TV Remote or close the remote control within the app. Live TV requires that the Argus TV server be sent a "keep alive" signal periodically, otherwise it will stop the RTSP stream. Argus TV Remote will take care of sending the "keep alive" signal as long as the remote control window is open. You can, however, turn the screen off on your device and Argus TV Remote will continue running in the background.

### Note on Battery Usage

After casting a recording or live TV stream from your device to Kodi, Argus TV Remote will continue to run in the background and monitor the recording as long as you leave the remote control window open. This occurs even if you switch apps or turn off the screen on your device. This is necessry to display program and time info, and to update the last played position in Argus TV. If you are concerned about battery usage, you can turn off this monitoring by closing the remote control window either by selecting the "X" button on the remote, or closing the notification that appears when a recording is being monitored.
