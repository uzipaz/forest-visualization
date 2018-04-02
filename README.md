# forest-visualization

In this project, we are given thousands or more data points that we wish to visualize with 3D objects in each frame and we are required to optimize the rendering performance as much as possible. We can achieve this by using GPU supported instanced rendering that improves performance.

In our dataset, each row contains characteristics and a position that represents a tree in a forest. There are just over one thousands of trees in a single time frame, as we go along the axis of time in our dataset, the characteristics of the trees changes. These changes represents the lifetime or trees in a forest. Graphically visualizing this data can help us easily spot abnormalities, any unusual characteristics or just study a group of trees in the forest. 

Using GPU instancing becomes very important here because we can represent a tree with a single mesh but there are potentially thousands or millions of trees in a forest and it is not feasible to call the draw function for every individual tree object since it can cause performance bottleneck because of CPU to GPU communication when calling a draw function.

In our project, we use WebGL which is OpenGL API in Javascript for rendering graphics on any compatible web browser. Rendered graphics are displayed inside a webpage as an HTML canvas object.

