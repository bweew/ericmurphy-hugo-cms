+++
draft = false
date = '2023-12-26 18:56:32'
title = "how to vectorize"
description = "converting jpg to scalable vectors using potrace in the terminal or even better, this web app"
slug = "raster-to-svg"
tags = ["vectorize", "terminal"]
+++

# potrace
its a terminal app that takes bmp as input and exports eps
```
potrace bird.bmp -o bird.eps
``` 
# svgcode
this webapp uses wasm to run potrace in the browser
i found this shortly after potrace so i didn't stick around to learn all the cli options. but i like how under algorithm option: they have one called "turdsize" -t supress speckles of up to this size (default 2)

{{< youtube id="kcvfyQh6J-0" title="SVGcode: A PWA to convert raster images to SVG vector graphics" >}}

[link to the webapp svgcode](https://svgco.de/)

# stable diffusion auto svg
{{< youtube id="6dQAn9I43o8" title="🤯Generate Mindblowing SVG/Vector art in Stable Diffusion | AUTOMATIC1111 Guide" >}}
