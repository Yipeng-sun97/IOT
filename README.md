  # *21/11/2020

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



