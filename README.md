haus-lan
========

### This repo explains how to render a text-only diagram to raster image, e.g. PNG

#### You need
* [ditaa](http://ditaa.sourceforge.net/)
* [jre](http://www.oracle.com/technetwork/java/javase/downloads)

### First you draw the diagram with ASCII text characters
```
+---------------------------------------------------------------------+
|                                                                     |
|   Objects                                                           |
|                                                                     |
|   +-----------------+               +---------+                     |
|   |parallelogram{io}|               |rectangle|                     |
|   +-----------------+               +---------+                     |
| Network fabric provider    Infrastructure services provider         |
|                                                                     |
| /----------------------\               +----=------+                |
| | four rounded corners |               |dashed edge|                |
| \----------------------/               +----=------+                |
|     Network Client           Normally detached from network         |
|                                                                     |
| /----------------------+                                            |
| |  two rounded corners |                                            |
| +----------------------/                                            |
|     Embedded system                                                 |
|                                                                     |
+---------------------------------------------------------------------+
|{d}                                                                  |
|   Connectors                                                        |
|                                                                     |
|     <---> IP over wired          *---* Ethernet over wired          |
|                                                                     |
|     <-=-> IP over wireless       *-=-* Ethernet over wireless       |
|                                                                     |
+---------------------------------------------------------------------+
```
### Second you generate the image with ditaa like this
`$ ditaa haus-lan.txt`

### Which produces a PNG like this!
![Example network diagram legend](https://github.com/qrkourier/haus-lan/blob/master/EXAMPLE.png)
