## NO INSTRUMENT YET MEASUREMENT

**INTRODUCTION**

**PROBLEM SUMMARY**

It is very difficult to measure the dimensions of any object without the instruments, so we are going to solve the problem using modern computer vision technology which can help us to measure the dimensions like height and width of the objects. Also, we will be adding features to measure area, distance, angle etc. of an object in measurable unit (such as millimeter, inches, etc.).

**AIM AND OBJECTIVES**

The purpose of this object is to provide functionalities to user, so they can measure the structured and unstructured objects without using any measurement tools and also it can be used in robots to get dimensions of the objects and many more.

**PROBLEM SPECIFICATION**

Measure the dimensions of object is difficult without any physical instrument so by this project we are going to solve this problem using computer vision technology which can help us to measure the dimensions like height, width of object Also, we will be adding features to measure area, distance, angle etc. of an object in measurable unit (such as millimeter, inches, etc.).

**MATERIALS/TOOLS REQUIRED**

**Technology Stack:**

**Python programming language:**

Python is an interpreted high-level programming language for general-purpose programming.It provides constructs that enable clear programming on both small and large scales.

**PyCharm Software:**

PyCharm is an integrated development environment (IDE) used in computer programming, specifically for the Python language. It provides code analysis, a graphical debugger, an integrated unit tester and integration with version control systems (VCSes).

**Computer Vision (OpenCV):**

OpenCV (Open Source Computer Vision) is a library of programming functions mainly aimed at real-time computer vision. The library is cross-platform and free for use under the open-source BSD license.

**Vuforia SDK:**

Vuforia is an augmented reality software development kit (SDK) for mobile devices that enables the creation of augmented reality applications. It uses computer vision technology to recognize and track planar images (Image Targets) and simple 3D objects, such as boxes, in real time. This image registration capability enables developers to position and orient virtual objects, such as 3D models and other media, in relation to real world images when they are viewed through the camera of a mobile device.

**ARCore:**

ARCore is Google&#39;s platform for building augmented reality experiences. Using different APIs, ARCore enables your phone to sense its environment, understand the world and interact with information. Some of the APIs are available across Android and iOS to enable shared AR experiences.

**Hardware**

**Camera**
**Android Smart Phone**

**IMPLEMENTATION**

**Calculate Measurement (Pythagorean Theorem)**

&quot;We use Pythagorean Theorem for measure the objects&quot;

![Untitled](https://user-images.githubusercontent.com/36161491/102871550-927cc180-4464-11eb-8c52-22e76b23bf9e.png)

**Fig.1 Graph of Pythagorean Theorem**

Graphing in xyz-space can be difficult because, unlike graphing in the xy-plane, depth perception is required. To simplify plotting of points, one can make use of projections onto the coordinate planes. The projection of a point (x; y; z) onto the xy-plane is obtained by connecting the point to the xy-plane by a line segment that is perpendicular to the plane, and computing the intersection of the line segment with the plane.

**The Distance Formula:**

The distance between two points P1 = (x1, y1) and P2 = (x2, y2) in the xy-plane is given by thedistance formula,

![Untitled2](https://user-images.githubusercontent.com/36161491/102871558-94468500-4464-11eb-83b9-c18e072c326a.png)

**Fig.1(a) Equation of Pythagorean Theorem**

Similarly, the distance between two points P1 = (x1, y1, z1) and P2 = (x2, y2, z2) in xyz-space is given by the following generalization of the distance formula,

![Untitled3](https://user-images.githubusercontent.com/36161491/102871560-94468500-4464-11eb-8b42-cdc85f91b781.png)

**Fig.1(b) Equation of Pythagorean Theorem**

This can be proved by repeated application of the Pythagorean Theorem. Example The distance between P1 = (2, 3, 1) and P2 = (8, -5, 0) is

![Untitled4](https://user-images.githubusercontent.com/36161491/102871567-96104880-4464-11eb-9467-ed8e6aadb816.png)

The final answer is in centimeter

Now we convert centimeters to meters with this simple formula:

**METERS = CENTIMETERS × 0.01**

Converting a centimeter length measurement to a meter measurement involves multiplying the length by the conversion ratio to find the result. One centimeter is equal to 0.01 meters, so to convert simply multiply by 0.01.

For example, here&#39;s how to convert 5 centimeters to meters using the formula above.

**5 cm = (5 × 0.01) = 0.05 m**

Centimeters and meters are both units used to measure length. Centimeters are a metric measurement and can be abbreviated as cm, for example 1 cm. Meters are a metric measurement and can be abbreviated as m, for example 1 m.

Internationally the centimeter is actually spelled centimeter and it&#39;s equal to 10 millimeters, .01 meters, or .393701 inches. Metric rulers have 30 cm and they are the larger measurement. A standard pencil is just about 1cm thick, and can be used to get a rough idea of the size of a centimeter.

The meter is the primary unit of length in the metric system. It&#39;s equal to 100 centimeters or 39.37 inches. Internationally it is actually spelled meter. It was first defined 1793 as 1/10,000,000 the length from the equator to the North Pole. The current definition of a meter, adopted in 1983, is the distance light travels in 1/299,792,458 seconds and was adopted to in 1983.

We recommend using a ruler or tape measure for measuring length, which can be found at a local retailer or home center. Rulers are available in imperial, metric, or combination with both values, so make sure you get the correct type for your needs.

**Augmented Reality**

&quot;We solved camera near-far problem using augmented reality&quot;

We use two types of augmented reality.

**Mark less Augmented Reality**
**Marker Based Augmented Reality**

Augmented reality (AR) is a type of interactive, reality-based display environment that takes the capabilities of computer-generated display, sound, text and effects to enhance the user&#39;s real-world experience.

Augmented reality combines real and computer-based scenes and images to deliver a unified but enhanced view of the world.

![Untitled5](https://user-images.githubusercontent.com/36161491/102871564-94df1b80-4464-11eb-96ff-e11c9fee6486.png)

**Fig.2 Augmented Reality**

**Surface Detection (Mark less Augmented Reality)**

We use mark less augmented reality for measure large scale object which is not fit into mobile screen.

It is does not need any pre-knowledge of a user&#39;s environment to overlay 3D content into a scene and hold it to a fixed point in space.

- **Environmental understanding**
- **Motion tracking**
- **Oriented points**

**Environmental understanding**

We use ARCore technology to improving its understanding of the real-world environment by detecting feature points and planes.

We look for clusters of feature points that appear to lie on common horizontal or vertical surfaces, like tables, floor, walls, and makes these surfaces available to your app as planes. We can also determine each plane&#39;s boundary and make that information available to your app. You can use this information to place virtual objects resting on flat surfaces.

Because we uses feature points to detect planes, flat surfaces without texture, such as a white wall, may not be detected properly.

![Untitled6](https://user-images.githubusercontent.com/36161491/102871571-96a8df00-4464-11eb-8c01-05ed57ebc428.png)

**Fig.3 AR Environment**

**Motion tracking**

As your phone moves through the world, we use a process called concurrent odometry and mapping, or com, to understand where the phone is relative to the world around it. We detect visually distinct features in the captured camera image called feature points and uses these points to compute its change in location. The visual information is combined with inertial measurements from the device&#39;s imu to estimate the pose (position and orientation) of the camera relative to the world over time.

![Untitled7](https://user-images.githubusercontent.com/36161491/102871573-97417580-4464-11eb-8127-bc067cd85970.png)

**Fig.4 Motion tracking**

**Oriented points**

Oriented points let you place virtual objects on angled surfaces. When you perform a hit test that returns a feature point, we will look at nearby feature points and use those to attempt to estimate the angle of the surface at the given feature point. We will then return a pose that takes that angle into account.

Because we use clusters of feature points to detect the surface&#39;s angle, surfaces without texture, such as a white wall, may not be detected properly.

![Untitled8](https://user-images.githubusercontent.com/36161491/102871575-97417580-4464-11eb-9873-41e8ed258be2.png)

**Fig.5 Oriented Points**

**Image Recognition (Marker Based Augmented Reality)**

Marker-Based AR is also called Image Recognition or Recognition based AR. In simple words, this technology uses the camera in AR device to produce a result. QR and 2D are the examples of the visual marker. The users get the result when camera reader senses the marker.

- **Augmented Images**
- **Multiple Image Target**

**Augmented images**

Augmented images are a feature that allows you to build ar apps that can respond to specific 2d images such as product packaging or movie posters. Users can trigger ar experiences when they point their phone&#39;s camera at specific images — for instance, they could point their phone&#39;s camera at a movie poster and have a character pop out and enact a scene.

Images can be compiled offline to create an image database, or individual images can be added in real time from the device. Once registered, we will detect these images, the images boundaries, and return a corresponding pose.

We use Vuforia SDK for solving the near far problem. We make 2D markers using Image Target

Image Targets are the easiest way to put AR content on flat objects, such as magazine pages, trading cards and photographs.

![Untitled9](https://user-images.githubusercontent.com/36161491/102871576-97da0c00-4464-11eb-9a2a-096b30b500a0.png)

**Fig.6 Marker Based AR**

**Multiple Image Target**

We create Multi Image Targets using more than one Image Target (Augmented Images) and can be arranged into regular geometric shapes (e.g. boxes) or in any arbitrary arrangement of planar surfaces.

![Untitled10](https://user-images.githubusercontent.com/36161491/102871581-9872a280-4464-11eb-8b38-00fd5e954e61.png)

**Fig.7 Multiple Image Target**

**Object Detection (OpenCV)**

We use OpenCV for Object Detection and Realtime Video Capture

- **Canny Edge Detection**
- **Contours**
- **Pixels Per Metric**

- **Canny Edge Detection**

The Canny edge detector is an edge detection operator that uses a multi-stage algorithm to detect a wide range of edges in images.

- **Noise Reduction:** remove the noise in the image with a 5x5 Gaussian filter
- **Finding Intensity Gradient of the Image:** Smoothened image is then filtered with a Sobel kernel in both horizontal and vertical direction

![Untitled11](https://user-images.githubusercontent.com/36161491/102871584-990b3900-4464-11eb-8471-d52b5d0a4b62.png)

- **Non-maximum Suppression:** full scan of image is done to remove any unwanted pixels which may not constitute the edge.

![Untitled12](https://user-images.githubusercontent.com/36161491/102871585-99a3cf80-4464-11eb-85d6-d323fef9fad0.png)

**Fig.8 Non maximum suppression**

- **Hysteresis Thresholding:** This stage decides which are all edges are really edges and which are not. For this, we need two threshold values, minVal and maxVal.

![Untitled13](https://user-images.githubusercontent.com/36161491/102871586-9a3c6600-4464-11eb-8c9f-b757feedc59b.png)

**Fig.9 Hysteresis Thresholding**

**Contours**

We use contours for a curve joining all the continuous points (along the boundary), having same color or intensity. The contours are a useful tool for shape analysis and object detection and recognition.

- For better accuracy, use binary images. So before finding contours, apply threshold or canny edge detection.
- find Contours function modifies the source image. So if you want source image even after finding contours, already store it to some other variables.
- In OpenCV, finding contours is like finding white object from black background. So, remember, object to be found should be white and background should be black.

![Untitled14](https://user-images.githubusercontent.com/36161491/102871590-9ad4fc80-4464-11eb-89c0-22d8ec18e62c.png)

- **The &quot;pixels per metric&quot; ratio**

In order to determine the size of an object in an image, we first need to perform a &quot;calibration&quot; (not to be confused with intrinsic/extrinsic calibration) using a reference object. Our reference object should have two important properties:

Property #1: We should know the dimensions of this object (in terms of width or height) in a measurable unit (such as millimeters, inches, etc.).

Property #2: We should be able to easily find this reference object in an image, either based on the placement of the object (such as the reference object always being placed in the top-left corner of an image) or via appearances (like being a distinctive color or shape, unique and different from all other objects in the image). In either case, our reference should be uniquely identifiable in some manner.

In this example, we&#39;ll be using the United States quarter as our reference object and throughout all examples, ensure it is always the left-most object in our image:

![Untitled15](https://user-images.githubusercontent.com/36161491/102871591-9b6d9300-4464-11eb-8261-e816c2e9d1a5.png)

**Fig.10 Pixel per metric ratio**

By guaranteeing the quarter is the left-most object, we can sort our object contours from left-to-right, grab the quarter (which will always be the first contour in the sorted list), and use it to define our _pixels\_per\_metric_, which we define as:

_ **pixels\_per\_metric = object width / know\_width** _

A US quarter has a _known\_width_ of 0.955 inches. Now, suppose that our _object\_width_ (measured in pixels) is computed be 150 pixels wide (based on its associated bounding box).

The pixels\_per\_metric is therefore:

_ **pixels\_per\_metric = 150px / 0.955in = 157px** _

Thus, implying there are approximately 157 pixels per every 0.955 inches in our image. Using this ratio, we can compute the size of objects in an image.

**SNAPSHOTS**

- **Module 1**

![Untitled16](https://user-images.githubusercontent.com/36161491/102871595-9c062980-4464-11eb-9735-f3c062ab3d03.png)

**Fig.11 (a) Module 1 O/P**

![Untitled17](https://user-images.githubusercontent.com/36161491/102871597-9c9ec000-4464-11eb-94d8-794a2496506c.png)

**Fig.11 (b) Module 1 O/P**

![Untitled18](https://user-images.githubusercontent.com/36161491/102871602-9d375680-4464-11eb-8f5d-0d0c6e1d4a26.png)

**Fig.11 (c) Module 1 O/P**

- **Module 2**

![Untitled19](https://user-images.githubusercontent.com/36161491/102871604-9dcfed00-4464-11eb-9777-c2eff29b08e9.png)

**Fig.12 (a) Module 2 O/P**

![Untitled20](https://user-images.githubusercontent.com/36161491/102871607-9dcfed00-4464-11eb-908b-8436f0c3208a.png)

**Fig.12 (b) Module 2 O/P**

![Untitled21](https://user-images.githubusercontent.com/36161491/102871609-9e688380-4464-11eb-85f9-5dcc841a21e4.png)

**Fig.12 (c) Module 2 O/P**

![Untitled22](https://user-images.githubusercontent.com/36161491/102871614-9f011a00-4464-11eb-98dd-255ef64e4931.png)

**Fig.12 (d) Module 2 O/P**

![Untitled23](https://user-images.githubusercontent.com/36161491/102871618-9f99b080-4464-11eb-8ea5-92007db5b78a.png)

**Fig.12 (e) Module 2 O/P [VR]**

**Module 3**

![Untitled24](https://user-images.githubusercontent.com/36161491/102871620-a0324700-4464-11eb-9fa7-cf4cf3ca5c7e.png)

**Fig.13 (a) Module 3 O/P (in cm) Fig.13 (b) Module 3 O/P (in m)**

![Untitled25](https://user-images.githubusercontent.com/36161491/102871623-a0cadd80-4464-11eb-9488-09e9ab34b620.png)

**Fig.13 (c) Module 3 O/P (Multiple Points) Fig.13 (d) Module 3 O/P**

![Untitled26](https://user-images.githubusercontent.com/36161491/102871624-a1637400-4464-11eb-9fc7-bec1634e7320.png)

**Fig.13 (e) Module 3 O/P (Measure Height)**

**User Interface**

![Untitled27](https://user-images.githubusercontent.com/36161491/102871627-a1fc0a80-4464-11eb-97c7-0df18d3d524f.png)

**Fig.14 (a) User Interface O/P (Menu) Fig.14 (b) User Interface O/P (Help)**

1. **SUMMARY**

**4.1 SUMMARY OF RESULT**

We use camera for capture an image and Computer for Compute the data. The present invention is mainly directed to providing a method for calculating distance and method for accurately estimating a volume of an object and actual size of a small object.

  1. **ADVANTAGES OF YOUR WORK**

- **High product quality** : Incorporating continuous integration and daily testing into the development process, allowing the development team to address issues while they&#39;re still fresh.
- **Higher customer satisfaction** : Keeping customers involved and engaged throughout projects.
- **Increased project control:** Transparency
- **Reduced risks:** fell freedom when new changes need to be implemented. They can be implemented at very little cost because of the frequency of new increments that are produced.
- **Faster ROI** : freedom when new changes need to be implemented. They can be implemented at very little cost because of the frequency of new increments that are producedfeatures are delivered incrementally, therefore benefits are uforia early while the product is in development process.

  1. **CURRENT SCENARIO**

At a Present time, we must use specific instrument for measure specific object. Also, there are some Application is also available for measure an object, but that application is for specific device only because some devices only support some feature that help the calculate objects that&#39;s why this application support only few devices not in all devices.

  1. **FUTURE SCOPE**

NIYM system which is use camera and computer (at development phase) for all measurement. If we use Cloud platform for computation and we send the image using mobile to a cloud and on the cloud, we can do computation and get a result, so we can develop mobile compatible Application

  1. **UNIQUE FEATURES**

- Works on different environments and light conditions (e.g. low light)
- Ability to measure transparent objects like: glass
- Ability to measure small object like: screw, coin
- Ability to measure large objects which are not fit into mobile screen like: wall, floor
- Construct 3d environment only scan area so memory utilization is increased
- Converted into mixed reality so user can feel realistic
- Measure up to 1km
- User can generate multiple points for object measurement

**REFERENCES**

[https://docs](https://docs/).opencv.org/2.4/index.html

[https://blogs](https://blogs/).unity3d.com/2017/11/16/dealing-with-scale-in-ar/

[https://docs](https://docs/).opencv.org/3.1.0/d9/db7/tutorial\_py\_table\_of\_contents\_calib3d.html

[https://library](https://library/).vuforia.com/articles/Training/getting-started-with-vuforia-in-unity.html

[https://docs](https://docs/).opencv.org/3.1.0/da/d22/tutorial\_py\_canny.html

[https://developers](https://developers/).google.com/ar/develop/unity/quickstart-android

[https://docs](https://docs/).opencv.org/3.0.0/d4/d73/tutorial\_py\_contours\_begin.html

- **PATENT DRAFTING EXERCISE (PDE)**

![Untitled28](https://user-images.githubusercontent.com/36161491/102871631-a294a100-4464-11eb-821e-b813961511fa.png)
![Untitled29](https://user-images.githubusercontent.com/36161491/102871632-a32d3780-4464-11eb-99a0-9d2813b2680b.png)

