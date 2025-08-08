# Trappy-Scopes for Yeast People

<img src="/Users/byatharth/code/Trappy-Scopes/protocols/external/41579_2019_274_Figa_HTML.png" alt="Yeasts and how they came to be | Nature Reviews Microbiology" style="zoom:50%;" />



## How to image?

1. Select the right microscope:

	1. Every screen is multiplexed in the lab. You will be using the `VWR` microscope, which is on:

		+ Screen channel: `**HDMI**`
		+ HDMI multiplexer channel: **1** (but its always here)
		+ USB Keyboard channel: **2**
		+ Mouse: **There is a dedicated mouse.**

	2. Open the terminal **(if it is not open already)**:
		```bash
		cd            # -> go to home
		cd scope-cli  # -> go to trappy-scopes
		./trappyscope # -> Launch software
		## Press enter to skip setting up an experiment
		```

	3. There is a dedicated function to click images for you:

		```python
		yeast_capture_AG(sample, tsec=10, force=False)
		yeast_capture_MV(sample, tsec=10, force=False)
		```

		`sample`: sample name :: example - "yeast_strain__image1"

		`tsec`: Number of seconds of preview before capture. You can also press `Enter` to capture the image immediately.

		`force`: force rewrite of the image. The software would prevent using the same sample name twice (within the same minute). In case you need to retake the image, pass `force=True`.

		**This function (``yeast_capture...`)will do the following things:**

		1. Log you in - it knows who you are :skull_and_crossbones:
		2. Set up the specific experiment - your data directory.
		3. Sync the images to your server folder.

	4. Take the image:

		1. Find the FOV with the eye-piece before calling this function. 
		2. **Then refocus the image for the camera during the preview.** 
		3. If the FOV is tilted, adjust the camera gently.
		4. You can also use the preview on the screen if you dislike using the eyepiece:

		```python
		scope.cam.preview(30) ## start a 30 seconds preview
		scope.cam.preview(300) ## start a 30 seconds preview
		```

		To prematurely end the preview, go to the terminal and press `Ctrl+C`.If you feel like it, do the following (but it is not necessary):

		```python
		yeast_packup()
		```

	5. The images are already in your server folder. You can download it from there (IGC wifi or VPN needed):

| AG                                                           | MV                                                           |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| http://172.22.63.19:5000/sharing/80r93prSA                   | http://172.22.63.19:5000/sharing/fBF6O5iid                   |
| ![TS_VWR__AG__persistent_experiment-QRcode](/Users/byatharth/code/Trappy-Scopes/protocols/external/TS_VWR__AG__persistent_experiment-QRcode.png) | ![TS_VWR__MV__persistent_experiment-QRcode (1)](/Users/byatharth/code/Trappy-Scopes/protocols/external/TS_VWR__MV__persistent_experiment-QRcode (1).png) |

