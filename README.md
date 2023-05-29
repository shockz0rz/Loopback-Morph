# Loopback-Morph (for A1111 Webui)
Forked from https://github.com/FizzleDorf/Loopback-Wave-for-A1111-Webui .

This script is intended to be an enhanced version of the original Loopback Wave script, allowing finer control over aspects of the generation process with features inspired by the Deforum animation utility, while avoiding the huge number of features that make Deforum difficult to use for users looking for a "fancier Loopback Wave".

### Current features:

* Negative prompt scheduling - change your negative prompt at a target frame just like your positive prompt!

### Feature roadmap:

* **NEXT PRIORITY**: Alternative denoising strength strategies - select between "Cosine Spike" (the original Loopback Wave function), "Sinewave", "Linear", and "Flat".

* Mask switching: Change the inpaint mask at a specified frame, or switch between inpainting and full Img2Img.

* Video frame interpolation: Make smoother output videos

* ??

## Original README by FizzleDorf
Img2img Loopback with Denoise controls over designated frames. This is modified to work with the latest Stable Diffusion Webui updates including changed to the output directory management. If you are using an older version, pull from the [original branch](https://github.com/FizzleDorf/Loopback-Wave-for-A1111-Webui/tree/original) or the original code on the rentry provided in this README.

*Disclaimer: I am not the original author of this script. This was originally by an anonymous user on 4chan I came across during my early months exploring animations in SD. There is no "official" repo, only the rentry page linked in this README*

![yGUEhcG](https://user-images.githubusercontent.com/46942135/232080320-a53a5373-14ef-40b8-99c7-3ae97141cc33.gif)

Original rentry by anon where you can find the original script: https://rentry.org/sd-loopback-wave

My rentry guide explaining how it works: https://rentry.org/AnimAnon-LoopbackWave

Installation:
Place the script into the A1111 webui Scripts folder. The script will become a selection in the script dropdown. This only works in the img2img tab and also requires an input image to use. Explainations of the settings are in the two links provided above.


I hope you have fun with it! Feel free to fork and edit the code but I will not be accepting PRs unless there is something completely broken that needs to be fixed.
