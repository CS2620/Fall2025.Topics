# Fall2025.Topics
The topics that are covered each day during class
- [You can find the notes from class here](https://uofnebraska-my.sharepoint.com/:f:/g/personal/17816140_nebraska_edu/EktuKJi3m_9Khf6sZLG_lrkBc46ZoPAOI6gCk86_xmf0sQ?e=sRqveC)
- [You can find previous semesters' final videos here](https://www.youtube.com/playlist?list=PLH9qo0GKu2iSlchbSeksN18S87gMIjHOg)


# Day 02, August 28 - Grayscale

## Review
- What is the difference between your cornea and your lens?
- What is the difference between your cones and your rods?

## Editing an image
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



## Anatomy-conscious grayscale
- There are an infinite number of ways to convert to grayscale, consider https://cs2620.github.io/grayscale/
- NTSC: 0.2126 ∙ Red + 0.7152 ∙ Green + 0.0722 ∙ Blue (https://en.wikipedia.org/wiki/Grayscale)

## Color isolation/Selective Color
- Examples of professional art: https://www.nicholasgooddenphotography.co.uk/london-blog/selective-colour-photography

## Create a image of colors
- Code at https://github.com/CS2620/Fall2025.Day02.Grayscale/blob/main/02-color-swatch.py

## Bayer Filtering
- Eyes != Cameras
  - Additional information at https://en.wikipedia.org/wiki/Bayer_filter
- Demosaicing
  - Additional information at https://en.wikipedia.org/wiki/Demosaicing

## Ideas to explore on your own


# Day 01, August 26 - Eye Anatomy

## What kinds of computer graphics are we going to use?
- Watch trailer, https://www.youtube.com/watch?v=-sAOWhvheK8
- What different kinds of computer graphics are there?
    - See slides on computer graphics
- What a trailer, what image processing is used? https://www.youtube.com/watch?v=iV46TJKL8cU

## Eye anatomy
- See slides on eye anatomy
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

## Final code
```python
# If you do not have pillow installed, you may need to run the following from the command line: `python -m pip install pillow`
from PIL import Image

image = Image.new("RGB", (100, 100))

image.save("./black.png")
```
