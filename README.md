# mp4 to m3u8 ts hls video
The windows batch scripts that generate m3u8 playlists from h264 mp4 video for Apple HLS, using ffmpeg.


## Dependency and preparation
### ffmpeg
#### 1 Download ffmpeg for windows. 
You can donload it from [ffmpeg.org](https://www.ffmpeg.org/download.html#build-windows), or [here](https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-full.7z) is a direct link to the latest release in .7z compressed file.
#### 2 Install (copy) the ffmpge to your PC. 
Just uncompresse the 7z or zip you've got and copy the folder including all files to a clear location like `c:\ffmpeg\ `
#### 3 Add your ffmpeg path to system environment variables
Windows 10: 
* Just type `advanced system settings` in your task bar search, open it.
* Goto tab "Advanced", go stright down to "Environment Variables"
* Find "Path" in the top "User variables for [username]", double click the "Path" line.
* Click "New" and input your ffmpeg path including the bin folder. For example: `C:\ffmpeg\bin`.
* Then click OK all the way down to save your change.

Windows 7:
* You can find the "Advanced system settings" by right click "Computer" on your star menu or explorer and click `Properties`.
* Goto tab "Advanced", go stright down to "Environment Variables"
* Find "Path" in the top "User variables for [username]", double click the value of "Path" line.
* Move your cursor to the end of the value of "path", Don't delete anything what's already in there.
* Add your ffmpeg path start with a semicolon, like `....xxx;C:\ffmpeg\bin`
* Click OK to save your change.

#### 4 verify ffmpeg works
* Open CMD (Commend Prompt)
* Type `ffmpeg` and Enter
* If the cmd didn't say it's an unknown command, you are good to go.


## How to use

