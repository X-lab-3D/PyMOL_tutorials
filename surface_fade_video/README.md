1) Fetch 1oga structure
2) Create one object for each chain, e.g.:
```create mhc_a, chain='A'```
3) Set colors and visualizations (e.g. sticks) as preferred. Show the surfaces.
4) Choose a starting position. Save it as scene 001:
Either on the menu, Scene-->Append or on command line:
```scene 001, store```
5) Choose a second, more zoomed-in position. Save it as scenne 002 (as above)
6) Click on scene one. Make a roll movie (Menu, Movie-->Program-->Camera loop--> Y-Roll --> 8 seconds)
7) Click on scene two. Repeat as in point 6 (do a Camera loop Y Roll)
8) Identify the two keyframes that merge the two programs on the bottom blue line. It will be the "chubby" one. If you play the video, you can see how there is not a nice interpolation between them.
9) Use ctrl + shift + right click to drag one of these two frames away from the others (wither the first one to the left or the second one to the right). Just move them away a bit.
10)(optional) Use ctrl + shift + left click and drag from left to right to add frames (green bar will be shown) between these two keyframes.
11) Download the [movie_fade.py script](https://raw.githubusercontent.com/Pymol-Scripts/Pymol-script-repo/master/movie_fade.py) Run the movie_fade.py script. [Explanation here.](https://pymolwiki.org/index.php/Movie_fade)
12) Run ```import movie_fade```
13) identify a starting and a ending frame for your fading. I suggest as starting the keyframe where the movie starts zooming and as ending frame somewhere during the final rolling of the video.
14) the movie fade command should be: ```movie_fade <setting>, <startFrame>, <startValue>, <endFrame>, <endValue>``` so, assuming you selected frames 240 and 380 as start and end, run:
```movie_fade transparency, 240, 0., 380, 0.9```
15) Before you save the video, you want to reset the surface transparency. This is a session-wide value that will be maintained at the beginning of your saved video, so it's important to reset it. Go to the beginning of the movie. Set again transparency to 0:
```set transparency, 0```
16) Save your file: Menu, File--> Export Movie as --> Select the best option for your sytem (mp4/MPEG4 is lighter than GIF, but a bit less universal. Do not use PNG images as that will literally generate one png for each frame of the video.)




https://user-images.githubusercontent.com/55996385/173611362-63226319-f6fb-439a-8f9f-fcf195e49aa5.mp4
