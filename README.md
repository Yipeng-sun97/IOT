  # *21/11/2020 to 25/11/2020
  # little project

## Play the music on raspberry pi by python

##  using pygame
```
from  pygame import mixer  # Load the popular external library 

mixer.init()
mixer.music.load('e:/LOCAL/music/love.mp3')
mixer.music.play()
```

## install the pygame library before you use it.
```
pip3  install  pygame
```

This library has limited support for MP3 files, and its website states that it may crash under Debian, on which the official Raspberry Pi system is based, so this method is not recommended. For more information, please refer to this website [pygame](http://www.pygame.org/docs/ref/music.html)

## using vlc Python binding modules
```
pip3 install python-vlc         #Python3
```
```
sudo apt-get install vlc -y  
```
after that, I should install pulseaudio
```
import vlc
p = vlc.MediaPlayer("file:///path/to/track.mp3")
p.play()
```
when I want to stop play
```
p.stop()
```

But, there are some problems.
```
[0a27ad50] vlcpulse audio output error: PulseAudio server connection failure: Connection refused
[0a351e20] vlcpulse audio output error: PulseAudio server connection failure: Connection refused
```
Finally, I deal with this problem
The way to solve the problem
```
rm -r ~/.pulse
rm -r ~/.pulse-cookie
rm -r ~/.config/pulse
sudo pulseaudio -k
pulseaudio --start
```
## Raspberry Pie - WeChat Music Player
This version is relatively simple, and some new features have been extended to RasWxMusicbox during this period, such as support for logging in to one's NetEase cloud music account, support for playing one's own favorite song list, etc. Specific features include.

H: Helpful Information

L: Login to Netease Cloud Music

U: User song list

M: Playlist

N: Next song

R: Now Playing

S: Song Search

T: Hot Singles

E: Exit


Raspberry Pie WeChat Music Player, using Netease Cloud Music API, based on itchat WeChat framework. I learn much from [this](https://github.com/littlecodersh/ItChat). 
Then, I watch the [Demo Video](https://v.youku.com/v_show/id_XMTYwMDkzOTk4MA==.html#paction)




# Project
## Access to Ali Platform

Turn on the IoT IoT Suite [Ali] (https://www.aliyun.com/product/iot) 

The properties corresponding to the object model are reported to the payload.
```
{
    id: 123452452,
    params: {
        temperature: 26.2,
        humidity: 60.4
    },
    method: "thing.event.property.post"
}
```
# Device Side Development
```
$ pip install paho-mqtt
```
Analog Device Thermometer.py Code

# Equipment Startup
```
$ python thermometer.py
```

