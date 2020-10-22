---
title: "Image processing with dynamic linking"
collection: portfolio
created: April 2020
order: 1010
---
Image Processing with Dynamic Linking is a project about processing images using plugins that are dynamically linked. The program developed in the project take an image and applies a specified plugin to the image. The program loads the image and dynamically calls the specified plugin to process the image.

I developed the following plugins:
- swapbg - a plugin that generates an image with swaped blue and green values for each pixel in the input
- mirrorh - a plugin that generates a horrizontally reflected image of the input
- mirrorv - a plugin that generates a vertically reflected image of the input
- tile - a plugin that generates an N x N arrangement of tiles, each tile being a smaller version of the original image, and the overall result image having the same dimensions as the original image
- expose - a plugin that generates an image where all red, blue, and green values from the input image are multipled by a constant

The program also checks what plugins are available and lists them uses the `list` command-line parameter.

Here are some exmaples of what the program and plugins do:

This is the original image (by [latch.r](https://www.flickr.com/photos/lachlanrogers/), [some rights reserved](https://creativecommons.org/licenses/by-sa/2.0/)):
![A kitten](/images/portfolio/dynamic_image_kitten.png)

This is the result of applying the swapbg plugin to the image:
![The result of applying the swapbg plugin to the kitten image](/images/portfolio/dynamic_image_kitten_swapbg.png)

This is the result of applying the mirrorh plugin to the image:
![The result of applying the mirrorh plugin to the kitten image](/images/portfolio/dynamic_image_kitten_mirrorh.png)

This is the result of applying the mirrorv plugin to the image:
![The result of applying the mirrorv plugin to the kitten image](/images/portfolio/dynamic_image_kitten_mirrorv.png)

This is the result of applying the tile plugin to the image with parameter N=2:
![The result of applying the tile plugin to the kitten image](/images/portfolio/dynamic_image_kitten_title.png)

This is the result of applying the expose plugin to the image with parameter 0.5:
![The result of applying the expose plugin to the kitten image](/images/portfolio/dynamic_image_kitten_expose.png)
