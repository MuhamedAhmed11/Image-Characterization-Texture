# Image Characterization using Texture
The texture is an important image feature used in many computer vision systems. In this 
coursework, we will analyze and implement one of the most common statistical methods to extract 
texture descriptors: co-occurrence matrices. They are fast and easy to implement and provide 
good results that could be used in a posterior step to perform image segmentation and object 
recognition/classification. 

Regarding the final objective, texture can be computed globally or locally. By globally, it is 
understood that all pixels in the image are used to compute a final vector of features. In contrast, 
locally means that texture is computed at each pixel by using just its neighborhood. Hence, each 
pixel will have its own vector of features. In this coursework, we will develop both approaches. 
Firstly, the goal is to be able to create output images corresponding to different texture descriptors. 
Therefore, we will apply the co-occurrence matrices at the local level producing descriptors for 
each pixel. We will then use these descriptors to enhance the Region Growing segmentation 
algorithm. 

## Part I - Feature Vetor

&nbsp;
## Part II - Region Growing
In this Report we test 4 images [feli.tif](./Captures/feli.tif), [hand2.tif](./Captures/hand2.tif), [mosaic8.tif](./Captures/mosaic8.tif), and [pingpong2.tif](./Captures/pingpong2.tif).
For each image we generate four images first  with added two planes, then two different images with only one plane for each image, and last one is without any added planes.

### **2.1. feli.tif**
| **1-Image without any Added Planes** | **2-Image with Added Two Planes** |
|:-------------:|:-------------:|
| ![without-any-planes](./Captures/Problem2/feli/output1-without-planes.jpg) | ![with-two-planes](./Captures/Problem2/feli/output1-with-two-planes.jpg)|

| **3-Image with only one plane** | **4-Image with another Plane** |
|:-------------:|:-------------:|
| ![without-first-planes](./Captures/Problem2/feli/output1-first-plane.jpg) | ![with-second-planes](./Captures/Problem2/feli/output1-second-plane.jpg)|

> Comment: As shown, First image without adding any planes got slightly the best result as it separted the object from the background without overfitting also we can differentiate the boundaries of the object from backgorund

&nbsp;
### **2.2. hand2.tif**
| **1-Image without any Added Planes** | **2-Image with Added Two Planes** |
|:-------------:|:-------------:|
| ![without-any-planes](./Captures/Problem2/hand2/output2-without-planes.jpg) | ![with-two-planes](./Captures/Problem2/hand2/output2-with-two-planes.jpg)|

| **3-Image with only one plane** | **4-Image with another Plane** |
|:-------------:|:-------------:|
| ![without-first-planes](./Captures/Problem2/hand2/output2-first-planes.jpg) | ![with-second-planes](./Captures/Problem2/hand2/output2-second-plane.jpg)|

> Comment: As Shown First and Fourth Images got the best results. but, First image got better results compared to fourth as Hand appears as one object except one finger in both images. So, First Image without adding any Planes got best result as we can differentiate that there are 3 objects (Hand, Rotating Circle suspended with Finger, and the background) but It detects one finger as a whole object which is false.

&nbsp;
### **2.3. mosaic.tif**
| **1-Image without any Added Planes** | **2-Image with Added Two Planes** |
|:-------------:|:-------------:|
| ![without-any-planes](./Captures/Problem2/mosaic/output3-without-planes.jpg) | ![with-two-planes](./Captures/Problem2/mosaic/output3-with-two-planes.jpg)|

| **3-Image with only one plane** | **4-Image with another Plane** |
|:-------------:|:-------------:|
| ![without-first-planes](./Captures/Problem2/mosaic/output3-first-plane.jpg) | ![with-second-planes](./Captures/Problem2/mosaic/output3-second-plane.jpg)|

> Comment: As the image is separated into four quarters it's difficult to tell that there is a best result for the four quarters (whole image) since each result gives the best result for specific quarters. But, We can choose the Third Result (Image with only one plane) is the best because it differentiates between the four quarters in a good way as the rest result images make two quarters as one object this clearly appears in the first image that mix the objects in the upper right quarter with lower right quarter also appears in the second result image that mix (can't differntiate) between upper two quarters.

&nbsp;
### **2.4. pingpong2.tif**
| **1-Image without any Added Planes** | **2-Image with Added Two Planes** |
|:-------------:|:-------------:|
| ![without-any-planes](./Captures/Problem2/pingpong2/output4-without-planes.jpg) | ![with-two-planes](./Captures/Problem2/pingpong2/output4-with-two-planes.jpg)|

| **3-Image with only one plane** | **4-Image with another Plane** |
|:-------------:|:-------------:|
| ![without-first-planes](./Captures/Problem2/pingpong2/output4-first-plane.jpg) | ![with-second-planes](./Captures/Problem2/pingpong2/output4-second-plane.jpg)|

> Comment: First Image without adding any planes got the best results as we can fine differntiate between the objects in the image (Hand, ping-pong paddle, ball, table, and the background)