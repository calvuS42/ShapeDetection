# ShapeDetection
Assesment for the summer Computer vision internship. The program detects shapes (triangles, rectangles and circles) on the piece of paper in the video.

The output video can be found down below:

https://user-images.githubusercontent.com/31920760/127781548-1e2e09a5-5f32-4385-81a0-25b80abbaffc.mp4

The main task of object detection was divided into several parallel subtasks. Since it was decided to use separate built-in algorithms to detect circles and figures with angles, each frame of the video should be processed differently. The problem was the uneven illumination throughout the entire video and additional noise that appeared on the texture outside the specified area.

During the image preprocessing phase for both algorithms, the color map of the image was changed to HSV. This was due to the fact that in high brightness conditions the yellow and white colors blend together, making it impossible to clearly distinguish the edge. The transition to a different color scheme allowed to highlight the saturation of colors of the figure, which contributed to the highlighting of edges in the image. Further, for different algorithms different image processing techniques were applied. An interesting detail that is important to mention was the use of a mask filter which helped to highlight a more homogeneous space. 

Unfortunately, the chosen method and parameters give false positive results in some cases, which can be seen on the video.
