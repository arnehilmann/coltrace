# coltrace

col(or)trace: convert color image to vector graphics (based heavily on potrace and Imagemagick)

sharp edges when zooming, transparent background, smaller size (often)


## examples/logo

<img src="https://raw.githubusercontent.com/arnehilmann/coltrace/master/examples/logo.jpeg" width="400px"/><img src="https://raw.githubusercontent.com/arnehilmann/coltrace/master/examples/logo.jpeg.zoomed.png" width="200px"/>
<br/>
<img src="https://raw.githubusercontent.com/arnehilmann/coltrace/master/examples/logo.color.svg?sanitize=true" width="400px"/><img src="https://raw.githubusercontent.com/arnehilmann/coltrace/master/examples/logo.svg.zoomed.png" width="200px"/>


## tl;dr

```
$ git clone https://github.com/arnehilmann/coltrace.git

# on MacOS
$ brew install gnu-sed potrace imagemagick || brew upgrade gnu-sed potrace imagemagick

$ cd coltrace
$ bin/coltrace examples/logo.jpeg
$ open out/logo/index.html
```


## usage

```
coltrace SOURCE [POSTERIZE [WIDTH]]

    SOURCE          input image; assumption: white background, good contrast, no noise
    POSTERIZE       number of colors per channel (default 3)
                    2: 8 unique colors, 3: 27 colors, 4: 64 colors
    WIDTH           width of svg (default 24cm)


env parameters:
    RENDER_COLOR    should color svg be rendered (default true)
    DEBUG           debug output (default true)
```
