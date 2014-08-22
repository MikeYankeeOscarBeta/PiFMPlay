PiFMPlay
========
Its an addon for pifm(a program to transmit FM-Radio) for the raspberry pi mini computer.

PiFMPlay makes it easier to play music and control your FM-Broadcast.

PiFM is written by [Icrobotics](http://www.icrobotics.co.uk/wiki/index.php)

PiFMPlay is written by Mikael Jakhelln.
"It's not pretty, but i works."

##How to use it:
Put pifmplay on your pi (e.g /home/pi).

Allow it to be run as a program:
>sudo chmod +x pifmplay

>sudo chmod +x pifm

Install sox and ffmpeg with:
>sudo apt-get install ffmpeg sox libsox-fmt-all 

Attach an antenna to GPIO4 on your raspberry pi.

###Test it:

>sudo sh pifmplay . 91.3

(91.3 is the default frequency, change it to whatever frequency you want to broadcast on.)

###Play a file with:

>sudo sh pifmplay "/path/to/file.mp3"

>sudo sh pifmplay "/path/to/file.m4a"

>sudo sh pifmplay "/path/to/file.wav"

this will play a file with pifm.

###Play from a pipe

>cat /path/to/file | sudo pifmplay PIPE

to play a file locally (the cat command only being an example here).

>cat <audio file> | ssh pi@raspberrypi 'cat - | sudo /home/pi/pifmplay/pifmplay PIPE'

play a file from your local pc over ssh on the raspberry pi.

###Play a folder with:

>sudo sh pifmplay "/path/to/folder" 101.5

###How to Pause/Stop broadcast and skip songs:
Open another terminal.

>sudo sh pifmplay pause

>sudo sh pifmplay resume

>sudo sh pifmplay stop

>sudo sh pifmplay next

To control pifmplay from the same terminal, run pifm in the background:
>sudo sh pifmplay "/path/to/folder" &
(tho you might want to remove the text output)

Check if there is an update to pifm here: 
[icrobotics.co.uk](http://www.icrobotics.co.uk/wiki/index.php/Turning_the_Raspberry_Pi_Into_an_FM_Transmitter)


####Things I would like to see pifmplay do in the future:
- Redirect all sound output to pifmplay (redirect all alsa sound output).
- Youtube stream (might be possible with [youtube-dl](http://www.raspberrypi.org/phpBB3/viewtopic.php?p=97710))
- di.fm/soundcloud/spotify/pandora streaming

####If you get in troube using this, IT'S ON YOU:
The raspberry pi can be made into a powerful fm-transmitter, if you filter and amplify the signal. 
But using a powerful fm-transmitter without a proper licence is illegal in most countries.
So if you break any laws and get fined for it, it's YOUR OWN FAULT!!
But it should be fine as long as you don't attach a big antenna to it.
