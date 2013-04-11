Ideas for the [Recording Studio](../../exhibits/recording-studio) exhibit
===========================================================================

Initial thoughts
-------------------

Sratch the Rasberry Pi, I have a first gen AppleTV that needs a new purpose in life.

Could we hook up the camera to an AppleTV with gentoo linux on it. 

Use the current joysticks connected to the same servos as we already have.

Maybe embed the wussy looking webcam into a more impressive looking 'shell'?

On the Gentoo distro I have on my appletv, mplayer would do the trick nicely:

  * http://en.gentoo-wiki.com/wiki/Webcam#Recording

Combine them, encode them as mp4 and upload them using the python boto library to an S3 bucket.

Display the unique ID for the video on the screen. 

Maybe use a simple label printer to print out a "redemption ticket" that has the unique id of the video on it? 

  * http://code.google.com/p/python-escpos/
  * Epson POS Thermal Receipt Printer - Model TM-T88III - USB on Ebay for ~$130-150

We could also enable different "modes" so you can manually control the camera, or flip a switch and do [face tracking](http://mitchtech.net/raspberry-pi-servo-face-tracker/), in case everyone wants to be in the box.

We'd need a way to split the video output over multiple screens. And we'd also need to make sure that whatever was cooked up for software required the least amount of user or staff input.

We'd also need to do three things when the record button is pressed:

  1. Start recording from the webcam
  2. Start recording from the mic
  3. Start playing the selected track

Once the session is over, we'd have to:

  1. Extract the audio from the mp4 file
  2. Mux the music track with the audio and add it to the stripped m4v file

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

HDMI splitter: http://www.monoprice.com/products/product.asp?c_id=101&cp_id=10113&cs_id=1011306&p_id=8153&seq=1&format=2

Muxing audo tracks with video files: http://ubuntuforums.org/showthread.php?t=1504282
