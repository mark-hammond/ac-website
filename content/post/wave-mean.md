+++
title = "Wave-Mean Flow Interactions in the Atmospheric Circulation of Tidally Locked Planets"
date = 2018-10-26T15:19:18+01:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = []

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = []
categories = []

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
# Use `caption` to display an image caption.
#   Markdown linking is allowed, e.g. `caption = "[Image credit](http://example.org)"`.
# Set `preview` to `false` to disable the thumbnail in listings.
[header]
# image = "gcm-sim.png"
# caption = "55 Cancri e GCM Simulation"
# preview = false

+++

Our paper on wave-mean flow interaction on tidally locked planets has been accepted by ApJ – here’s the preprint!


<!--more-->

This work was mostly prompted by two fantastic papers, [Showman (2011)](https://www.lpl.arizona.edu/~showman/publications/showman-polvani-2011.pdf) and [Tsai (2014)](https://arxiv.org/pdf/1405.0003.pdf), which used shallow-water models to understand the global atmospheric circulation of tidally locked exoplanets (one side always faces the star it orbits). 

GCM simulations of these planets look something like:

![Example image](/img/gcm-sim.png)

The problem is that this doesn`t look much like the shallow-water model that should correspond to a tidally locked planet ([Matsuno (1966)](http://employees.oneonta.edu/ellistd/meteorology/matsuno1966.pdf)). Here is the response to forcing in zero background flow.

![Example image](/img/ps-no-flow.png)

The hot spot is in the wrong place compared to the GCM, as are the cold lobes at high latitudes.

### Effect of Equatorial Jet

The key thing missing from this solution is the equatorial jet that forms on these planets ([Showman (2011)](https://www.lpl.arizona.edu/~showman/publications/showman-polvani-2011.pdf)). [Tsai (2014)](https://arxiv.org/pdf/1405.0003.pdf) showed that a uniform flow could shift the waves making up this pattern eastwards. 

We changed this to a non-uniform jet on the equator, and added the fact it is balanced by a pressure perturbation. Here is the respose in a shear background flow.

![Example image](/img/ps-shear-flow.png)

This matches the GCM simulations at the top better. The nice thing about this method was that we were solving one set of equations for one solution, rather than previously where I had summed different solutions together.

### Scaling Laws

We also solved the problem in a spherical geometry, rather than on the mathematically nice beta-plane approximation. This matches the GCM output more closely, and represents the rotation rate better.

This meant we could show the effect of different parameters on the solution. For example, a slow planetary rotation rate looks like:

![Example image](/img/sp-g-30.png)

and a fast rotation rate looks like:

![Example image](/img/sp-g-003.png)

The main difference is caused by the fact that the pressure perturbation from the jet is linearly proportional to the rotation rate. We look at a few more ways the parameters affect the circulation in the paper.

We were prompted to understand this circulation better when trying to interpret the phase curve of 55 Cancri e. This sort of model could be useful for observers trying to interpret different phase curves and eclipse maps.
