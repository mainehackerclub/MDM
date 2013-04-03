Ideas for the [Recording Studio](../../exhibits/recording-studio) exhibit
===========================================================================

Initial thoughts
-------------------

Rasberry Pi is awesome.

Could we hook up the camera to an RP device, use the current joysticks connected to some servos and save the video stream to an mp4 video file that gets saved directly to a S3 bucket?

We could also enable different "modes" so you can manually control the camera, or flip a switch and do [face tracking](http://mitchtech.net/raspberry-pi-servo-face-tracker/), in case everyone wants to be in the box.

We'd need a way to split the video output over multiple screens. And we'd also need to make sure that whatever was cooked up for software required the least amount of user or staff input.

Basic flow
------------

  1. Approach exhibit
  2. Select a song from a pre-loaded list of tracks
  3. Press a nice and obvious "start recording" button
  4. Use a joystick to pan/tilt a camera
  5. When the song finishes playing
    a. prompt user for email address to send link to video
    b. Ask if they'd like a DVD burned downstairs
  6. Restart the software loop

Considerations
----------------

What would the interface look like? Small digital readout? Full-fledged PC or TV monitor?

It'd need some sort of keyboard for email input. 

Need to look for easy-to-program servos to control camera movement. Some resources:

http://www.doctormonk.com/2012/07/raspberry-pi-gpio-driving-servo.html

http://projectsmax246.blogspot.co.uk/2013/01/webcam-over-3g-with-raspberry-pi.html

http://mitchtech.net/raspberry-pi-servo-face-tracker/

https://github.com/richardghirst/PiBits/tree/master/ServoBlaster
