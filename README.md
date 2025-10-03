# Fall2025.Topics
The topics that are covered each day during class
- [You can find the notes from class here](https://uofnebraska-my.sharepoint.com/:f:/g/personal/17816140_nebraska_edu/EktuKJi3m_9Khf6sZLG_lrkBc46ZoPAOI6gCk86_xmf0sQ?e=sRqveC)
- [You can find previous semesters' final videos here](https://www.youtube.com/playlist?list=PLH9qo0GKu2iSlchbSeksN18S87gMIjHOg)


# Day 11, October 02 - Hue, Saturation, and Value (🧑‍🏫Lecture 👟Sprint)


## 💡New Idea: HSV

## 👩‍💻Activity: Saturation in film
- Find Colors
- Also look at Encanto
- [Dorothy Entering Oz](https://www.youtube.com/watch?v=x6D8PAGelN8)
- [Wes Anderson Color Palette](https://www.youtube.com/watch?v=JQoNhRN9CiI)
- [Speed Racer Color Palette](https://www.youtube.com/watch?v=3FtBAGMSw-I)
- Look for H,S,V changes in this clip: [Mission Impossible 3, look at last clip](https://www.youtube.com/watch?v=N_7zkF2XnAA)


## 🧭Ideas to explore on your own
- What other color spaces are there or should there be
- What are the strengths and weaknesses of HSV?


## 🏁Final Code
 - [The final code for today](https://github.com/cs)
<br/><br/>
---
---


# Day 10, September 30 (👟Sprint)

<br/><br/>
---
---

# Day 09, September 25 - Interpolation (🧑‍🏫Lecture)

## 🔙Review
- Linear Interpolation
  - Interpolating between points $(0, A)$ and $(1, B)$ where the desired x is $p$, then the answer is found with: $(1-p)A+pB$

## 💡New Idea: Nearest Neighbor Interpolation
- In nearest neighbor interpolation, a final color is chosen by selecting the known pixel center closest to the interpolated coordinate.
- Nearest neighbor interpolation preserves original colors, edges aren't blurred, but it suffers from strong aliasing
- Additional information can be found on this [Wikipedia Article About Nearest Neighbor Interpolation](https://en.wikipedia.org/wiki/Nearest-neighbor_interpolation)

## 👩‍💻Code Together: Nearest Neighbor Interpolation
- Implement nearest neighbor interpolation while scaling to show the distinct artifacts it creates

## 📺Video: Nearest Neighbor Interpolation in Early Video Games
- This kind of interpolation was used in classic video games
  - For example, look for nearest neighbor interpolation in this video of [Wolfenstein 3D](https://www.youtube.com/watch?v=MnjXHOApVIc)

## 💡New Idea: Bilinear Interpolation
- We can use linear interpolation on a 2D image by:
  - Interpolating between the top two pixels (horizontally)
  - Interpolating between the bottom two pixels (horizontally)
  - Interpolating between the results (vertically)
- Bilinear interpolation can introduce new colors into the interpolated image. It tends to smooth sharp edges but has less aliasing than nearest neighbor interpolation
- Additional information can be found on this [Wikipedia Article About Bilinear Interpolation](https://en.wikipedia.org/wiki/Bilinear_interpolation)


## 💡New Idea: Bicubic Interpolation
- Cubic interpolation fits a degree 3 polynomials to four points to create a better fit than linear interpolation.
- Bicubic interpolation can be done by interpolating four times horizontally and one time vertically
- Bicubic interpolation tends to preserve sharp edges better than linear interpolation without introducing the same aliasing as nearest neighbor interpolation
- As a reminder, you can do cubic interpolation with the following code:
```python
return [
        1/6*(-A+3*B-3*C+D)*factor**3+ 
        1/2*(A-2*B+C)*factor**2+
        1/6*(-2*A-3*B+6*C-D)*factor+
        B
        for A, B, C, D in zip(negativeOne, zero, one, two)]
```
- Additional information can be found on this [Wikipedia Article About Bicubic Interpolation](https://en.wikipedia.org/wiki/Bicubic_interpolation)
- Additional information can be found on this [Wikipedia Article Comparing Types of Interpolation](https://en.wikipedia.org/wiki/Comparison_gallery_of_image_scaling_algorithms)

## 👩‍💻Code Together: Bilinear and Bicubic Interpolation
- Create a program that generates an animated image of an image being rotated.
- Do the rotating with bilinear interpolation and then bicubic interpolation.
- Compare the results.

## 📺Video: Enhance, Enhance, Enhance
- There are limitations to what can be done with interpolation. 
- During an NFL game, the broadcaster zoomed up on a player's foot. This video shows what is actually possible with interpolation. For example, the grass does not become crisper when the image is scaled. [Video of 2024 Chiefs Game Showing Interpolation](https://www.youtube.com/watch?v=Lteh13M2U70)
- In this fictional show, a computer user is able to "enhance" an image to show things that were not original visible. This is not possible with interpolation. [Video of Fictional Enhancement using Interpolation](https://www.youtube.com/watch?v=I_8ZH1Ggjk0)
  

## 🧭Ideas to explore on your own
- What would happen if you did interpolation using a higher degree polynomial, for example a degree five polynomial?
- What other ways of interpolating can you think of?


## 🏁[Today's Final Code on GitHub](https://github.com/CS2620/Fall2025.Day09.Interpolation)

<br/><br/>
---
---



# Day 08, September 23 (👟Sprint)

<br/><br/>
---
---


# Day 07, September 18 - Interpolation Prep (🧑‍🏫Lecture)

## ~~📢Announcements~~


## 🔙Review
- Quick review of transforms
- [Liquid Glass Release](https://www.youtube.com/watch?v=jGztGfRujSE)

## 👩‍💻Activity: Discuss Apple's Liquid Glass Design 
- You can see the full design specification here: https://developer.apple.com/documentation/technologyoverviews/liquid-glass
- Are icons difficult to see in tinted mode? Why?
- Can we explain why using eye anatomy?
  - Consider rods and cones


## 💡New Idea: Histograms
- A histogram shows the frequency of different levels in an image.
  - Additional information at https://en.wikipedia.org/wiki/Image_histogram
- What does a histogram tell us about an image?
- What 'should' a histogram look like?
- 🛝See slides about Histograms

## 👩‍💻Activity: Histograms
- Generate a histogram from a specific image.
- Compare the histograms of different Liquid Glass homescreen modes.
  - Do they appear the way we would expect?


## 💡New Idea: Major File Formats
- Photographers led to JPG (JPEG)
- Online led to GIF and then PNG
- There has been a recent support for animated PNGS
- 🛝See slides about File Formats

## 👩‍💻Activity: Create an animated image
- View an animated PNG we create ourselves
- Compare to the animated results from a GIF

## 💡New Idea: 1D Linear Interpolation
- To interpolate between color and BW, we need to interolate
- Linear interopolation results in the following formula:
$$(1-x)A+xB$$
- 🛝See slides about Sampling



## 🧭Ideas to explore on your own
- How would you improve Liquid Glass to be easier use?
- Are there other ways to quantify the effectiveness of a design language besides histograms?

## 🏁Final Code
 - [The final code for today](https://github.com/cs)
<br/><br/>
---
---

# Day 06, September 16 (👟Sprint)

<br/><br/>
---
---

# Day 05, September 11 - Advanced Transforms (Lecture)

## 📢Announcements
- Sprint next week
- Quiz prep
  - Review major topics from the previous weeks

## 🔙Review
- Which matrix does a vertical flip
- What matrices do the following transformations?
  - Translate
  - Scale
  - Rotate

## 👩‍💻Activity: Horizontal Flips
- Use what we learned in class last time to determine the matrix for a horizontal flip
$$
\begin{bmatrix}
-1 & 0 & w-1 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

## 💡New Idea: Translate
$$
\begin{bmatrix}
1 & 0 & dx \\
0 & 1 & dy \\
0 & 0 & 1
\end{bmatrix}
$$
- 🛝See slides about Translate

## 💡New Idea: Scale
$$
\begin{bmatrix}
sx & 0 & 0 \\
0 & sy & 0 \\
0 & 0 & 1
\end{bmatrix}
$$
- 🛝See slides about Scale
- When we scale up, this creates a series of black lines.
- The solution is...


## 💡New Idea: Push v Pull
- We want to pull pixels into the new image, not push pixels from the original image
- This prevents gaps and creates better images
- However, we need to use the inverse of our matrices, $M^{-1}$

## 💡New Idea: Basic Rotations
$$
\begin{bmatrix}
cosine(\theta) & -sine(\theta) & 0 \\
sine(\theta) & cosine(\theta) & 0 \\
0 & 0 & 1
\end{bmatrix}
$$
- This rotates an image about the origin. 
- How do we rotate about the center of the image?

## 💡New Idea: Centered Rotations
- Translate so the center of the image is at the origin
- Rotate
- Translate so the center of the image returns
- 🛝See slides about Rotation

## 💡New Idea: Rotation canvas size
- How should the canvas be resized when we rotate?
- We can expand the canvas if we rotate the four corners and find their difference in x and y

## 🧭Ideas to explore on your own
- What other transforms are there?
- How can we make our transforms (especially rotations) less grainy?


## 🏁Final Code
- :octocat: [Advanced Transformations](https://github.com/CS2620/Fall2025.Day05.AdvancedTransforms)


<br/><br/>
---
---

# Day 04, September 9 - Transforms

## 📢Announcements
- Upcoming sprints
  - Review the list of sprint ideas on the syllabus
  - It is fine to reimplement something we have done in class
  - If you have questions about what to do during the sprint, ask the teacher

## 🔙Review
- Write a simple color isolation algorithm on your own

## 💡New Idea: Transforms
- How can we change the shape, size and orientation of images?
- Is there a mathematically-sound way to do this for all transformations?
- 🛝See slides about Flips

## 👩‍💻Activity: Implement a vertical flip (flip over horizontal axis)
- What formula flips pixels over a horizontal axis?
  - `height-1-y`
- We need an second image otherwise we overwrite data

- See final code

## 💡New Idea: Matrix-based Transforms
- What basic transforms can we create with matrices?
  - Move (Translate)
  - Flip and resize (Scale)
  - Rotation
- Homogenous coordinates
- 🛝See slides about basic transformations

## 👩‍💻Activity: Implement a vertical flip using matrices
- Identify the matrix that will accomplish this transform
  - Flip over y (negative scale in the y direction)
  - Move `height-1`
- See final code

## 🧭Ideas to explore on your own
- What matrices would create other transformations?
- What transformations are not possible with matrices?

## 🏁Final Code
-  :octocat: [Transformations with and without matrices](https://github.com/CS2620/Fall2025.Day04.Transforms)
  


<br/><br/><br/>
---
---
# Day 03, September 3 - Bayer Filter & Demosaicing

## 📢Announcements
- Upcoming sprint
- Attend the career fair if possible
- 
## 🔙Review
- What is a better gray scale conversion? What makes a gray scale conversion good?


## 💡New Idea: Bayer Filtering
- Eyes != Cameras
- Digital cameras use a Bayer Filter to capture color images
  - Additional information at https://en.wikipedia.org/wiki/Bayer_filter
- Notably, images captured with a Bayer Filter only have one channel of information per pixel.

## 👩‍💻Activity: Bayer Filtering 
- Simulate a Bayer Filter on a given image

## 💡New Idea: Demosaicing
- In order to create an image with three channels of information (R,G,B), we need to transform a bayer filter image
- This process is called demosaicking.
  - Additional information at https://en.wikipedia.org/wiki/Demosaicing

## 👩‍💻Activity: Demosaicing
- What would a good demosaicing algorithm look like?
- Write a simple demosaicing algorithm by reducing the size of the image

## 🧭Ideas to explore on your own
- Are there better demosaicing algorithms?
- Are there better Bayer Filter layouts?
- Could we improve hardware in such a way that we don't need Bayer Filtering?

## 🏁Final Code
- [Bayer Filter Simulation and Demosaicing](https://github.com/CS2620/Fall2025.Day03.BayerFilterhttps://github.com/CS2620/Fall2025.Day03.BayerFilter)
  
<br/><br/><br/>
---
---
# Day 02, August 28 - Grayscale

## 🔙Review
- What is the difference between your cornea and your lens?
- What is the difference between your cones and your rods?

## ~~📢Announcements~~


## 👩‍💻Activity: Editing an image
- Where to get images?
  - Stick with public domain (or equivalent) content
- Import in image in python
  - Code at https://github.com/CS2620/Fall2025.Day02.Grayscale/blob/main/00-import-image.py
- What is a pixel
  - Additional information at https://en.wikipedia.org/wiki/Pixel
- Loading the raster grid
  - Additional information at https://en.wikipedia.org/wiki/Raster_graphics
- Looping over the pixel grid
- Editing a pixel
  - Code at https://github.com/CS2620/Fall2025.Day02.Grayscale/blob/main/01-grayscale-image.py

## Syllabus
- Including sprints

## 💡New Idea: Anatomy-conscious grayscale
- There are an infinite number of ways to convert to grayscale, consider https://cs2620.github.io/grayscale/
- NTSC: 0.2126 ∙ Red + 0.7152 ∙ Green + 0.0722 ∙ Blue (https://en.wikipedia.org/wiki/Grayscale)


## 🧭Ideas to explore on your own
- Play around with selective coloring. Can you make an artistic image more artistic with our code?
- What if you wanted to select a specific color, but only in a particular part of the image? Could you do that?
- ## Color isolation/Selective Color
- Examples of professional art: https://www.nicholasgooddenphotography.co.uk/london-blog/selective-colour-photography


## 🏁Final Code
- You can find [today's code on GitHub]()

<br/><br/><br/>

---
---
# Day 01, August 26 - Eye Anatomy

## ~~🔙Review~~

## ~~📢Announcements~~

## 👩‍💻Activity: What kinds of computer graphics are we going to use?
- Watch trailer, https://www.youtube.com/watch?v=-sAOWhvheK8
- What different kinds of computer graphics are there?
    - See slides on computer graphics
- What a trailer, what image processing is used? https://www.youtube.com/watch?v=iV46TJKL8cU

## 💡New Idea: Eye anatomy
- 🛝See slides on eye anatomy
- Eye placement
- Cornea
  - Additional information at https://en.wikipedia.org/wiki/Cornea
- Iris/Pupil
  - Addition information at https://en.wikipedia.org/wiki/Iris_(anatomy)
- Lens
  - Additional information at https://en.wikipedia.org/wiki/Lens_(vertebrate_anatomy)
- Vitreous Body
  - Additional information at https://en.wikipedia.org/wiki/Vitreous_body
- Retina
  - Additional information at https://en.wikipedia.org/wiki/Retina
- Optic Nerve
  - Additional information at https://en.wikipedia.org/wiki/Optic_nerve
- Blind Spot
  - Additional information at https://en.wikipedia.org/wiki/Blind_spot_(vision)
- Rods
  - Additional information at https://en.wikipedia.org/wiki/Rod_cell
- Cones
  - Additional information at https://en.wikipedia.org/wiki/Cone_cell

## 🏁Final Code
```python
# If you do not have pillow installed, you may need to run the following from the command line: `python -m pip install pillow`
from PIL import Image

image = Image.new("RGB", (100, 100))

image.save("./black.png")
```
