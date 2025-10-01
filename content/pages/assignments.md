---
content_type: page
description: This section describes the four homework assignments for the class.
draft: false
learning_resource_types:
- Assignments
ocw_type: CourseSection
title: Assignments
uid: 41d0b379-f7c4-4738-d6ab-994fa02224ed
---
This page describes the four homework assignments for the class. The final project with some example student work is presented on the {{% resource_link "2fcf5de0-b2b1-19ca-33d1-c6ff7c739036" "projects" %}} page.

- {{% resource_link "f6e2f5ef-9085-40d5-8c92-8b6c92d20c78" "Homework 1: Relighting" %}}
- {{% resource_link "94b15d06-b371-4689-b01e-def79524f97e" "Homework 2: Optics" %}}
- {{% resource_link "764201fc-0e3a-4129-bb0a-5042f2a1da5f" "Homework 3: Human Computer Interaction (HCI) using Multi-Flash Camera" %}}
- {{% resource_link "6ade3847-f7ef-4a59-9cb8-4a1650bbe8f5" "Homework 4: Multispectral Imaging" %}}

Graduate students (enrolled in MAS.531) will complete four homework assignments, while undergraduates (enrolled in MAS.131) will complete the first three of these assignments.

Students are encouraged to program in MATLAB® for image analysis. C++, OpenGL and visual programming may be needed for some hardware assignments.

The {{% resource_link "d3847996-7885-4dc9-b998-4abe57781973" "MAS.131/MAS.531 Flickr group pool" %}} contains some images produced by students for the assignments and final project.

## {{< anchor "HW1" >}}{{< /anchor >}}Homework 1: Relighting

Combine two photos by mixing the color channels. Take multiple photos by changing lighting and other parameters. Be creative. Then mix and match color channels to relight.

You can use these for inspiration:

- Haeberli, Paul. {{% resource_link "a6f607cf-b8de-4f50-aeb8-fa6c42b1c4c1" "*Synthetic Lighting for Photography*" %}}. January, 1992.
- Raskar, Ramesh, Adrian Ilie, and Jingyi Yu. {{% resource_link "0687d0d1-b9ae-4c9f-9596-e1d109b0b22c" "*Image Fusion for Context Enhancement and Video Surrealism*" %}}. Presented at NPAR 2004.

MATLAB resources:

- Sigmon, Kermit. {{% resource_link "32eb2828-aaed-405d-a2c6-96719b9842b6" "*MATLAB Primer*" %}}. 2nd ed., 1992.
- The MathWorks. {{% resource_link "38610421-a1be-44d0-a46d-7a6325b9d23b" "*Image Processing Toolbox*" %}}.

Create a Web page for all your homework assignments. The Web page for each assignment should at least have well commented source code, all input images, intermediate results and final output. Please include some description below each image.

Here is good example of how to assemble your homework into a Web page:

- "{{% resource_link "9560b295-19b8-4310-a8f3-c2b7529876c1" "The Vertigo Shot" %}}" from a Carnegie Mellon Computational Photography class (Fall 2008).

On your Webpage, you should have sourcecode and other details. Please include intermediate results, if any.

## {{< anchor "HW2" >}}{{< /anchor >}}Homework 2: Optics

Purpose: Playing with rays, lens, focus and creating see-through effects.

Select one of these three sub-assignments, based on your background and interests.

- Assignment 2A: Virtual Optical Bench: Modify software to shoot rays
- Assignment 2B: Lightfield Photography: Take photos, shift each photo and average (using Photoshop/HDRshop/Matlab/OpenCV/Flash/Java, whatever you like)
- Assignment 2C: Same as 2B but render input photos in software

### Assignment 2A. Virtual Optical Bench

We will study how rays can be propagated thru free space and optical elements. The basic idea is simple. Each ray is four dimensional: it has a position (x,y) + angle (theta, phi). For each element (free space, lens, mirror etc), there is a simple formula to 'transfer' the ray into a new ray:

- Wikipedia: {{% resource_link "21d20c1b-1cfb-472c-9ca6-167c09d23250" "Ray transfer matrix analysis" %}}.

Part 1

Use ray-matrix operations and the 'ray' class to create an interface similar to Andrew Adam's {{% resource_link "ac980cf7-d4f5-408d-b913-e8ce607b879e" "LensToy software" %}}. (Opens a Shockwave file, requires Adobe Flash Player)

You can directly start with his software or write your own in OpenGL or MATLAB.

Then add new elements such as (i) prism (ii) lenslet (iii) ability to change focal length of lens etc.

Part 2

The LensToy only draws rays but does not form an intensity image.

Create images of 3D and 2D objects. To compute intensity at a point, you have to add up radiance of all rays incident at that point. Show effects like depth of field using aperture or capture lightfield by selectively blocking the aperture.

### Assignment 2B: Lightfield Photography

Please read the Lightfield Camera papers very carefully.

- Bennett, W., et al. "{{% resource_link "dbd9abae-d9e8-4c66-af9e-82ef52c2eb50" "High Performance Imaging Using Large Camera Arrays" %}}." 2005.

Digital refocusing using photos taken by an array of cameras is easy. If you compute an average of all the photos, the digital focus is at infinity. If you shift each photo cumulatively, e.g. shift each photo a pixel with respect to its immediate left neighbor, and then compute an average, the focus plane is closer. This simple shift+add strategy is sufficient to achieve reasonable refocusing effects.

Part 1

Use only 16 images along the horizontal translation. You will test your code on this dataset.

Part 2

Translate camera and take photos at fixed distance intervals. Place the camera on a ruler (or create a Lego Robot) for precise positioning. You are trying to imitate a camera array. Ideally, control the camera using Remote Capture software from your computer. Take 16 photos. Choose objects with vibrant bright saturated colors. If you can't think of a scene, try this. The forground scene is a flat red colored paper with see through vertical stripes creating a FENCE. Background scene is a flat book cover or painting with very little red in it.

Part 3

Show refocusing and see-thru effects. See examples at the {{% resource_link "0572148a-b061-44f6-8641-98680eb52eef" "Stanford Light Field Archive" %}}.

Submit all input images, source code and output for each item. Use high depth complexity, colorful, point specular (sphere) objects. To create multiple camera views, you can also aim at an array of mirrors, put the camera on a robot or x-y platform. Be creative with camera configurations, maybe with very large baseline or with a microscope. You can also use unstructured positions and use a calibration target (or structure from motion or Photosynth software) to find the positions.

More projects are described at the Stanford Computer Graphics Laboratory's "{{% resource_link "0146a869-6d14-429c-84ab-2fdde8959221" "Light fields and computational photography" %}}" page.

Other ways to create lightfields include:

- Flatbed scanner + lenticulars — See Yang, Jason C. "A Light Field Camera For Image Based Rendering." Master's Thesis, MIT, 2000. ({{% resource_link "201d8b93-86fb-4bee-95b8-97a5f352d2b8" "PDF - 1.7MB" %}})
- Masks — See Veeraraghavan, A., et al. "{{% resource_link "4768f74a-9c8e-4927-95a3-de46a34bed40" "Dappled Photography: Mask Enhanced Cameras for Heterodyned Light Fields and Coded Aperture Refocusing" %}}." ACM SIGGRAPH 2007.

### Assignment 2C: Lightfield Photography (same as 2B) but with Input Photos Rendered in Software

Part 1: Programmable focus

Compute images with plane of focus at different depth (shift each photo by a specific amount successively and compute an average).

Output 1: Digitally focus at infinity (average of all photos)

Output 2: Digitally focus on back plane (shift some and average)

Output 3: Digitally focus on front plane (shift more and average)

This is the key part of this assignment: The Output2 should demonstrate a see-thru effect.

Part 2: Extra Credit and Completely Optional

Find depth of each pixel using max-contrast operator.

Produce see-through effect by eliminating foreground color pixels. For rejecting a given plane, instead of taking average of 16 values, take the majority vote. Median of 16 values will work in some cases, but the most common value will be a more robust choice. If there is no clear majority, i.e. if the most common count is say below 5, set the pixel to black.

Compute images with variable depth of field (Use fewer photos picked from near the center position. Fewer photos means a larger depth of field.)

Compute images with slanted plane of focus.

- Wikipedia {{% resource_link "7a366796-e8bf-40ee-be83-8f075f3d37ff" "Scheimpflug principle" %}}.
- Vaish, Vaibhav, et al. "{{% resource_link "964b8df5-9e40-47ba-9e8e-5b8500c2131f" "Synthetic Aperture Focusing using a Shear-Warp Factorization of the Viewing Transform" %}}." A3DISS (at CVPR), 2005.

Create new bokeh (point spread function).

## {{< anchor "HW3" >}}{{< /anchor >}}Homework 3: Human Computer Interaction (HCI) using Multi-Flash Camera

Track hand or finger using shadows from colored RGB lights, video camera.

Most of source code is available online; you will have to modify for your task. ({{% resource_link "8eaab753-cc80-4070-b7f3-223aa5faf26d" "GZ" %}})

References

- {{% resource_link "eca730e3-e9c4-4427-ba80-33a0ec82822d" "Kar-Han Tan’s Web site" %}}
- Raskar, R., K-H Tan, R. Feris, J. Yu, and M. Turk. "{{% resource_link "627ee397-4523-4dd2-bce0-8831ee6b3e20" "Non-photorealistic Camera: Depth Edge Detection and Stylized Rendering using Multi-Flash Imaging" %}}." *Proceedings of ACM SIGGRAPH*, August 2004. \[Includes source code\]
- {{% resource_link "70b40e0f-0e5e-4d5f-a258-dae78555fd6e" "Rogiero Feris' Web site" %}}
- Vaquero, D., R. Feris, M. Turk, and R. Raskar. "{{% resource_link "eec76a6f-bc11-4597-8152-ca61df1110f3" "Multiflash Imaging and Applications" %}}.”

Part 1:

- Turn on 1 LED at a time, take 3 (or 4) photos
- Find silhouette from shadow
- Do region filling to indicate (render) hand against textured background on table

Part 2:

- Turn on 3 LEDs: R, G, B
- From one photo, decompose 3 photos using RGB channels
- Find shadows, do region filling and find foreground

Extra credit:

- Let two hands overlap, find internal silhouettes (i.e. boundary between two hands), indicate the two hands in different color in rendering
- On table, have printed photos of hand (so ordinary camera will be confused) or other crazy texture

## {{< anchor "HW4" >}}{{< /anchor >}}Homework 4: Multispectral Imaging

### Option 1: Open ended

Your own choice … send me an email to get the approval. You can do some background work for your final project as HW 4 but this should be sufficiently different from your final project.

### Option 2: Wavelength and Color

You will use a multi-spectral database and create the appearance of objects under light sources with given color profiles.

{{< tableopen >}}{{< theadopen >}}{{< tropen >}}{{< thopen >}}
STEPS
{{< thclose >}}{{< thopen >}}
DESCRIPTIONS
{{< thclose >}}{{< thopen >}}
RESOURCES
{{< thclose >}}{{< trclose >}}{{< theadclose >}}{{< tbodyopen >}}{{< tropen >}}{{< tdopen >}}
Step 1
{{< tdclose >}}{{< tdopen >}}
Recover multiple wavelength bands of a scene (using online database)
{{< tdclose >}}{{< tdopen >}}

{{% resource_link "54329855-d597-446c-a6c9-1252eff5b7f0" "CAVE Multispectral Image Database" %}} with 31 bands

You should try on at least 2 datasets among the 5 sections of this set:

1. Lemon slices (and color chart) from the section "{{% resource_link "b212928d-5760-4008-9172-06dc95069cc4" "Real and Fake" %}}"
2. One other set of your choice

{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Step 2
{{< tdclose >}}{{< tdopen >}}
Get the wavelength profile of at least two light sources (e.g. mercury vapor and sunlight), using curves available online or computing the curve yourself using a spectroscope)
{{< tdclose >}}{{< tdopen >}}
Instructions to build your own spectroscope: Turricchia, A., and A. Majcher. “Amateur spectroscope.” ({{% resource_link "f0dd9382-621c-43cd-840f-1dbae63c4f45" "PDF" %}})
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Step 3
{{< tdclose >}}{{< tdopen >}}
Multiply each band of scene with corresponding intensity of light source in that band
{{< tdclose >}}{{< tdopen >}}

Graph of human eye spectral sensitivity, to estimate "red," "green," and "blue" target values ({{% resource_link "fb2fd004-dd64-4470-87d8-a8297a6f74f8" "JPG" %}})

More about eye response: Koren, N. "{{% resource_link "cddeb565-81b0-4a47-bb7e-ae0f9d603e84" "Color management and color science: Introduction" %}}"

{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Step 4
{{< tdclose >}}{{< tdopen >}}
Create a weighted combination for 'red', 'green' and 'blue' target values
{{< tdclose >}}{{< tdopen >}}
 
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Step 5
{{< tdclose >}}{{< tdopen >}}
Render the colored scene
{{< tdclose >}}{{< tdopen >}}
 
{{< tdclose >}}{{< trclose >}}{{< tropen >}}{{< tdopen >}}
Extra credit
{{< tdclose >}}{{< tdopen >}}
Create a Metamer (objects with two different wavelength profile that look the same in RGB under a light source with specific wavelength profile)
{{< tdclose >}}{{< tdopen >}}
{{% resource_link "f4add979-ab50-4692-ab58-3dc66ee449b5" "Metamer applet" %}}
{{< tdclose >}}{{< trclose >}}{{< tbodyclose >}}{{< tableclose >}}