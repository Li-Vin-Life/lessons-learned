# Project: Digitalize-Photos
  
## TL;DR
This project aims to help digitalize printed photos (Python + OpenCV).
  
## Introduction
This idea came to mind after visiting my parents. My mother created many photo albums in the past which are now sitting in a closet and take up space. Although looking through photo albums is something special, the thought of creating digital copies (i. e. for preservation) was born. Of course there are proprietary solutions for this exact use case - buying a photo scanner for example - but I wanted to create something that helps me digitalize our photos with the tools I have. 

The key concept is to take picutes of the analog images (in my case with my smartphone). 

## Initial Approach
The initial approach is just taking pictures of the photos which is the actual digitization step. In order to get relatively constant results, this requires similar parameters for every picture, i. e. distance to the analog picture. Therefore I would need to build a hardware device to hold the smartphone at a constant distance to the picture (distance actually changes from album-to-album and page-to-page) and would still need to manually crop some pictures, making all this a very time consuming operation. 

The goal is to make this process as simple as possible. 

&rarr; I decided to use Python with OpenCV. 

## Constraints
- Pictures have different formats/orientation/aspect ratios
- Pictures are inside the album and can't be removed
- Picture quality

