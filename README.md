PiFMPlay
========
Its an addon for pifm(a program to transmit FM-Radio) for the raspberry pi mini computer.

PiFMPlay makes it easier to play music and control your FM-Broadcast.

Pifm is written by [Icrobotics](http://www.icrobotics.co.uk/wiki/index.php)

Pifmplay is written by Mikael Jakhelln.

##How to use it:
Put pifmplay on your pi (e.g /home/pi).

Allow it to be run as a program:
>sudo chmod +x pifmplay

>sudo chmod +c pifm

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

###Play a file with:

>sudo sh pifmplay "/path/to/folder" 101.5

(this will play a file with pifm on frequency 101.5)

###How to Pause/Stop broadcast and skip songs:
Open another terminal.

>sudo sh pifmplay pause

>sudo sh pifmplay resume

>sudo sh pifmplay stop

>sudo sh pifmplay next

Also you might want to check if there is an update to pifm here: 
[icrobotics.co.uk](http://www.icrobotics.co.uk/wiki/index.php/Turning_the_Raspberry_Pi_Into_an_FM_Transmitter)

