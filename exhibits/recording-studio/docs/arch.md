Architecture
=============

After careful consideration, here's my proposed architecture.

Inventory
---------

  * 2x Raspberry Pis
  * 1x Video camera (exists)
  * 1x Mixer panel (exists)
  * 2x Monitors (exist, could use upgrades)
  * 4x Microphones (exist)

Software
----------
  * FFMpeg -- recording camera input, streaming?
  * PyKaroke
  * Raspian Linux
  
Raspberry Pi #1 -- Karaoke
---------------------------

Runs Raspian with pykaraoke installed.

Needs a user friendly interface.

  * User selects song from a list (trackball? mouse? touch?)
  * Big "start recording" button triggers play
  * Sends start signal to Video Pi to start recording
  * Sends end signal when video playback ends to stop recording

What songs? Only 30-45 second clips, okay to use commercial songs?

Raspberry Pi #2 -- Video
-------------------------

Outputs the camera input to a monitor outside the studio.

Takes audio input from mixer and video from camera.

Encodes both into an mp4 file.

Saves file to S3 bucket.

Could also stream mp4 to CloudFront for "live" broadcasts.

