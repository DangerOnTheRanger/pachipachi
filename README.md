Pachipachi - media server over SSH
==================================


What!?
------

Pachipachi is a media server that allows you to watch video (with sound) over SSH 
encoded with ASCII block characters for universal low resolution playback, or optionally
with SIXEL encoding for terminals that support it for high-resolution playback. Sound is
meant to be handled via `aplay` or any similar program to play a sound stream from the terminal.
In short, any standard Linux terminal is transformed to a full-fledged media player.


How!?
-----

The idea of streaming animated images over SSH isn't too involved, as long as the client and
server both have the necessary bandwidth for real time playback. The real trick is how to send
sound at the same time without any special client or anything like that, but UNIX has already
given us a separate data stream in the form of good old `stderr`; all we have to do is
send sound over `stderr` and have the user redirect it to their sound card via `aplay` or
some similar program, while video is displayed on `stdout`. The end result is decent
video playback using nothing but what you might find on a run-of-the-mill Linux installation.
SIXEL support is admittedly not exactly common, but anyone using a SIXEL-enabled terminal
should be rewarded with video quality rivaling what you'd get from a sane media server solution.


But why!?
---------

> We choose to [do unnecessarily difficult things], not because they are easy, but because they are hard.

To test my abilites.

