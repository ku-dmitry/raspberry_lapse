# raspberry_lapse

Based on: https://bitbucket.org/fotosyn/fotosynlabs/src/master/RaspiLapseCam/

Current version by default captures better resolution photos and has different naming template so that it is compatible with Vegas still sequence import right out of the box. It also captures 2 photos per minute instead of one.

# Installation

Copy raspberry_lapse.py to your raspberry OS installation
    sudo nano crontab

At the bottom of the script insert

    @reboot python /home/raspberry_lapse.py &

Of course change /home to the correct pathway where you have the script.

Save this script (CTRL + X) and "Y" Rebooting the device will mean this script executes. On testing I found that it needs a full shutdown before this will reliably work each time. So to reuse the device you'll need to log in, and perform a shutdown with

    sudo reboot

# Turning lapse off

By default it starts recording timelapses every time you power your Raspberry up.
If you want to turn it off for one session use `top` console command to find out the python process ID (PID)
Then just execute

    sudo kill PID
    
Have fun!
