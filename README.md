# Super-Mario-Sunshine-Cutscenes-Switch-2-GCM
Ported the cutscenes from the Nintendo Switch's Super Mario 3D All Stars version of Super Mario Sunshine to the Gamecube version of Super Mario Sunshine. 

The purpose for making this was that the original cutscenes on Super Mario Sunshine are 4:3. The Switch's version has 16:9 cutscenes that were re-rendered/edited for that version of the game. This has some caveats. This is not a 1:1 port of the Switch's cutscenes, they had to be downscaled to because the THP Converter I was using doesn't support 1280x720 as a resolution; must be too big or something for THP files. The resolution of these cutscenes is the same as the originals on Gamecube they're just 16:9 now, kind of a shame but I figured some compromises were to be made. The sound on the Switch cutscenes is missing from the files themselves because of how that game handles things differently; it just streams the audio in when it needs it. I used the audio from the gamecube version partly for this reason, and partly because the [audio for FLUDD explaining the Switch controls is different when explaining controls](https://www.mariowiki.com/Super_Mario_3D_All-Stars#Changes_to_Super_Mario_Sunshine) compared to the gamecube version.

This is something I wanted to do for a while but sat on because at the time I didn't really know what I was doing. I had some motiviation and figured I'd give it another shot. 

## How they look
![image](https://user-images.githubusercontent.com/45341450/213933419-1177f480-5469-4efd-9a12-7761f52ed26b.png)


## Installation
[Dolphin extract and repack games tutorial](https://www.youtube.com/watch?v=uK5HI6fQVK4)\
Follow the instructions in the video above and replace the .thp files in ``files\data``

## Files used to make this
[Dolphin](https://dolphin-emu.org/download/) needs to be used for extracting and repacking the game
I used [Foobar2000](https://www.foobar2000.org/download) for extracting the .wav from the original Gamecube's .mp4's
[VLC](https://www.videolan.org/vlc/download-windows.html) to convert the .thp to .mp4s and to lower the resolution for THP Converter later.
[ffmpeg](https://ffmpeg.org/download.html#build-windows) with this batch file:
``ffmpeg.exe -i "bath.mp4" -i "bath.wav" -c:v copy -c:a aac bath2.mp4 -y``\
bath.mp4 = switch version\
bath.wav = gamecube audio\
bath2.mp4 = exported file\
[THP Converter](https://github.com/Lord-Giganticus/THP-Conveter) for repacking the .mp4s back into .thp files.
