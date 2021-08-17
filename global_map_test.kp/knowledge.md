---
authors:
- Nate Miller
created_at: 2021-08-16 00:00:00
tags:
- knowledge
- example
title: Testing a knowledge repo
tldr: Nothing much to see here...just trying this out
updated_at: 2021-08-16 17:20:57.412565
---

# Basic Global Map

At GFW we use a set style and projections for our maps, based on our
visualization style guide. For global maps we use an Equal Earth
projection. We have add features to `fishwatchr` to make it convenient
to make global maps that fit this style and use a `ggplot`-style
interface

## Land

The default theme is a `dark` theme centered at longitude 0. We can
begin our map by using a land vector file.

``` r
ggplot() +
  geom_gfw_land()
```

    ## Linking to GEOS 3.7.2, GDAL 2.4.2, PROJ 5.2.0


### Specify center longitude

The center longitude can be changed with the `center` parameter. Using a
central longitude of 160 is nice for a Pacific map as it avoids cutting
Africa on the west and South America on the east.

``` r
ggplot() +
  geom_gfw_land(center = 160)
```