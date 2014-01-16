PiFMPlay
========
Its an addon for pifm(a program to transmit FM-Radio) for the raspberry pi mini computer.
This makes it easier to play and a music broadcast.
Pifm is written by [Icrobotics](http://www.icrobotics.co.uk/wiki/index.php)
Pifmplay is written by Mikael Jakhelln


##How to use it:
Attach an antenna to GPIO4 on your raspberry pi.

Put pifmplay on your pi (e.g /home/pi).

Allow it to be run as a program:
>sudo chmod +x pifmplay
>sudo chmod +c pifm

###Test it with: 
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

###How to Pause/Skip/Stop broadcast
Open another terminal.
>sudo sh pifmplay pause
>sudo sh pifmplay resume
>sudo sh pifmplay stop
>sudo sh pifmplay next

Also you might want to check if there is an update to pifm here: 
[icrobotics.co.uk](http://www.icrobotics.co.uk/wiki/index.php/Turning_the_Raspberry_Pi_Into_an_FM_Transmitter)

