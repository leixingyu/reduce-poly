## Poly Reduction Visualization

### Introduction
I was looking through some algorithm for generating LODs and find this paper from 1998: A Simple, Fast, and Effective Polygon Reduction Algorithm [http://pds26.egloos.com/pds/201402/12/11/gdmag.pdf]

The idea is to collapse vertices one by one. I successfully implement this in Maya, however, it takes a lot of time to process high poly mesh. An optimization is to compute to desire poly-count, store the vertex order and then re-construct the mesh all at once at the end.

### How To:

1. load the reduceCommand.mll

2. select the mesh you want to reduce (make sure it's full triangle with a mesh count less than 3,000)

3. execute the following command with the desired reduce rate
```python
import maya.cmds as cmds
cmds.reduceCmd(percentage=50)
```

### Demo:

![](https://github.com/sheldonlei/reducePoly/blob/master/polyreduce.gif)

Full Video: https://youtu.be/juwPpeyG7yg
