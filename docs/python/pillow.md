---
metaTitle: "Python - Pillow"
description: "Read Image File, Convert files to JPEG"
---

# Pillow



## Read Image File


```py
from PIL import Image

im = Image.open("Image.bmp")

```



## Convert files to JPEG


```py
from __future__ import print_function
import os, sys
from PIL import Image

for infile in sys.argv[1:]:
    f, e = os.path.splitext(infile)
    outfile = f + ".jpg"
    if infile != outfile:
        try:
            Image.open(infile).save(outfile)
        except IOError:
            print("cannot convert", infile)

```

