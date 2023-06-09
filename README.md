# Loopback-Morph (for A1111 Webui)
Forked from https://github.com/FizzleDorf/Loopback-Wave-for-A1111-Webui .

This script is intended to be an enhanced version of the original Loopback Wave script, allowing finer control over aspects of the generation process with features inspired by the Deforum animation utility, while avoiding the huge number of features that make Deforum difficult to use for users looking for a "fancier Loopback Wave".

### Current features:

* Negative prompt scheduling - change your negative prompt at a target frame just like your positive prompt!

* Alternative denoising strength functions - select between Cosine Spike (the original Loopback Wave function), Sinewave, Linear Spike, Linear Continuous, Sigmoid, Inverse Sigmoid, and Flat.

  * Cosine Spike: The original Loopback Wave function. Gradual increase in denoise strength through about the first quarter of a wave, then linear-ish increase to maximum at the halfway point, then linearish decrease until 3/4 through, then gradual decrease to mininmum. Takes a while to get up to even half of the maximum strength so it may spend a lot of frames making relatively minor changes. But it doesn't loiter at high strengths for long, so it's useful for avoiding too many drastic changes to the original pic.

  * Sinewave: Exactly what it says on the tin - a plain old sinewave from minimum strength at the beginning of a wave to maximum at 0.5, then back down to minimum. Gets up to useful denoise strengths faster than Cosine Spike, but also stays at relatively high strengths for longer periods of time - may result in too-drastic shifts away from the original image.

  * Linear Spike: Linearly increases strength with each frame up to a maximum halfway through the wave, then linear decrease down to minimum. Gets up to medium strength faster than Sinewave and doesn't stay at high strength for as long, but still stays at high strength longer than Cosine Spike. 

  * Linear Continuous: Linearly increases strength through the entire wave, then resets to minimum. Not super useful IMO, but maybe you can find a use for it!

  * Sigmoid: Stays at low strength for a while, then very quickly increases to near-maximum strength at about 1/4 through the wave, stays there until around 3/4 through, then quickly decreases back down to mininum. Could be useful if you have a high minimum denoise strength.

  * Inverse Sigmoid: My new favorite! Very quickly jumps up to about halfway between minimum and maximum and stays there for most of the wave, then jumps up to near maximum at close to the halfway point, then jumps back down to the halfway point. Keeps the 'spike' behavior of Cosine Spike that helps make major changes, but wastes less time at lower strength.

  * Flat: Just keeps your default denoise strength and ignores the 'maximum additional' slider. Basically the same as using the default Loopback script. May come in handy once future fancy features are implemented.

### Feature roadmap:

* **NEXT PRIORITY**: Mask switching: Change the inpaint mask at a specified frame, or switch between inpainting and full Img2Img.

* Denoise strength function switching: Change denoise strength and strength function at specified frames.

* Video frame interpolation: Make smoother output videos

* Inpaint smoothing: Repeated inpainting tends to create ugly, obvious borders even when adding blur to the mask. This seems like something that should be fixable.

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
