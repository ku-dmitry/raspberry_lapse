# raspberry_lapse

Based on: https://bitbucket.org/fotosyn/fotosynlabs/src/master/RaspiLapseCam/

Current version by default captures better resolution photos and has different naming template so that it is compatible with Vegas still sequence import right out of the box. It also captures 2 photos per minute instead of one.

# Installation
* Create a directory /home/timelapse chmod it to 777
* Copy raspberry_lapse.py to your raspberry OS installation chmod it to 777
* Make it run every time you power up the Raspberry

        sudo crontab -e

* At the bottom of the script insert

        @reboot python /home/raspberry_lapse.py &

* Of course change /home to the correct pathway where you have the script.

* Save this script 
* Rebooting the device will mean this script executes.

        sudo reboot
        or 
        systemctl reboot

# Turning lapse off

By default it starts recording timelapses every time you power your Raspberry up.
If you want to turn it off for one session use `top` console command to find out the python process ID (PID)
Then just execute

        sudo kill PID
    
Have fun!
