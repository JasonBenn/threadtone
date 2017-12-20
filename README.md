# ThreadTone | a halftone representation of an image made of thread

The process of generating an image with thread is an idea of [Petros Vrellis](http://artof01.com/vrellis/index.html). As I've documented [here](http://www.thevelop.nl/blog/2016-12-25/ThreadTone/) the process is comprised of three steps:
  
  * Image pre-processing (cropping, resizing, etc.)
  * Algorithm to place threads
  * In my case parsing the result to G-Code for automated fabrication

A set of two example images can be found below. Please refer to my [blog](http://www.thevelop.nl/blog/2016-12-25/ThreadTone/) for more details.

![Threaded portrait of Poetin](/assets/poetinThreaded.png "Threaded portrait of Poetin")

![Threaded portrait of Angelina](/assets/angelineThreaded.png "Threaded portrait of Angelina")

## Snippets

Thread all files in a folder
`for img in `ls ~/Desktop/`; do python threadTone.py ~/Desktop/$img; done`

Extract PNG frames from a movie
`ffmpeg -i ~/Desktop/haven.mov ./originals/haven-mov/frame-%03d.png`

Delete duplicate frames
`fdupes -dN .`
