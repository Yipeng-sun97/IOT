21/11/2020

Play the music on raspberry pi by python

using pygame

from pygame import mixer  # Load the popular external library

mixer.init()
mixer.music.load('e:/LOCAL/music/love.mp3')
mixer.music.play()
