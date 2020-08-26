We can play sounds on khawy by using SoundManager or the typedef SM. Ofcourse before we can call any sound we need to load them. You load them by overriding state's load and adding resources.add(SoundLoader("mySound") or resources.add(SoundLoader("myMusic",false)) for when you want to stream music and not uncompress it all at once.

We have two important functions to play sounds, playMusic and playFx. The main diference between them is that one is for playing music in loop(playMusic) and the other one, playFx is meant for playing single sounds (shoot, jump,etc)  


### Sound format
Kha expects the sound to be a .wav with sample rate: 44100Hz 16 bit. One way to transform a sound is to use Audacity, by exporting the audio as a "WAV(Microsoft) signed 16-bit PCM"