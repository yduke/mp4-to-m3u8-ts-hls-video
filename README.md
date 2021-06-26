# mp4 to m3u8 ts hls video
The windows batch scripts that generate m3u8 playlists from h264 mp4 video for Apple HLS, using ffmpeg.


## Dependency and preparation
### ffmpeg
#### 1 Download ffmpeg for windows. 
You can download it from [ffmpeg.org](https://www.ffmpeg.org/download.html#build-windows), or [here](https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-full.7z) is a direct link to the latest release in .7z compressed file.
#### 2 Install (copy) the ffmpge to your PC. 
Just uncompressed the 7z or zip you've got and copy the folder including all files to a clear location like `c:\ffmpeg\ `
#### 3 Add your ffmpeg path to system environment variables
Windows 10: 
* Just type `advanced system settings` in your task bar search, open it.
* Goto tab "Advanced", go straight down to "Environment Variables"
* Find "Path" in the top "User variables for [username]", double click the "Path" line.
* Click "New" and input your ffmpeg path including the bin folder. For example: `C:\ffmpeg\bin`.
* Then click OK all the way down to save your change.

Windows 7:
* You can find the "Advanced system settings" by right click "Computer" on your star menu or explorer and click `Properties`.
* Goto tab "Advanced", go straight down to "Environment Variables"
* Find "Path" in the top "User variables for [username]", double click the value of "Path" line.
* Move your cursor to the end of the value of "path", Don't delete anything what's already in there.
* Add your ffmpeg path start with a semicolon, like `....xxx;C:\ffmpeg\bin`
* Click OK to save your change.

#### 4 verify ffmpeg works
* Open CMD (Commend Prompt)
* Type `ffmpeg` and Enter
* If the cmd didn't say it's an unknown command, you are good to go.


## How to use
1. Your .mp4 video file have to be h264 or h265, other wise you will have to re-encode. 
2. Download and place the script to the same folder as your original .mp4 video file.
3. Drag your .mp4 file directly to the batch script.
4. The CMD window will show you the progress, wait until it's done.

## The result
The script will create a folder named "media" in the very same folder, structured as below
- **media**
	- **[the original video file name]**
		- **hls**
			- **[the original video file name].m3u8**  *The overall playlist*
			- **1080_out.m3u8** *The 1080p video playlist*
			- **720_out.m3u8**  *The 720p video playlist*
			- **480_out.m3u8**  *The 480p video playlist*
			- **360_out.m3u8**  *The 360p video playlist*
			- **1080_out1.ts**	*The 1080p splitted videos*
			- **1080_out2.ts**
			- ..
			- **720_out1.ts**  *The 720p splitted videos*
			- **720_out2.ts**
			- ..
			- **480_out1.ts**  *The 480p splitted videos*
			- **480_out2.ts**
			- ..
			- **360_out1.ts**  *The 360p splitted videos*
			- **360_out2.ts**
			- ..
			- **cover_h1.jpg**  *The 1080p screenshots from the video*
			- **cover_l1.jpg**	*The 720p-ish screenshots from the video*
			- **preview.gif** *The animated gif generated from the video*

The machine-generated covers and preview image may not be correct.

## Term of use
There is no term of use for this, you can download, edit, use and distribute this script for personal or commercial purpose freely.
