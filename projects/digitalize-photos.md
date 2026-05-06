# Project: Digitalize-Photos
  
## TL;DR
This project aims to help digitalize printed photos (Python + OpenCV).
  
## Introduction
This idea came to mind after visiting my parents. My mother created many photo albums in the past which are now stored in a closet and take up space. While browsing through photo albums is still a special experience, the question of preservation, accessibility and even space saving came up. Of course there are established proprietary solutions for this use case, such as dedicated photo scanners. However, I wanted to explore whether it was possible to achieve acceptable digitization quality using tools I already have, primarily a smartphone and software-based processing.

The core idea was to photograph the printed images and improve consistency post-processing.

## Problem Statement
The main challenge is digitizing large numbers of printed photos in albums in a way that is
- Time-efficient
- Consistent across different albums and pages
- Achievable without specialized hardware

## Initial Approach
The initial approach is simply taking pictures of each printed photo which itself is the actual digitization step. However, achieving consistent results requires controlling several variables for every picture, most prominently camera distance. One solution would be building a physical rig for my smartphone but even then the results wouldn't be consistent and would require manual cropping for many pictures. Very time consuming.

The primary goal therefore became reducing manual effort for post-processing as much as possible.

&rarr; I decided to use Python with OpenCV. 

## Constraints
- Pictures have different formats/orientation/aspect ratios
- Pictures are inside albums and can't be removed
- Picture quality

## Issues & Revisions
My first thought was to define a fixed border in my code for cropping which I instantly discarded because this would still require a fixed camera distance and each picture would've needed the same format. Therefore this idea would neither achieve my goal nor improve the process. Besides, it wouldn't make use of any detection methods, which is the key component for reducing the post-processing effort. 

A detection method that came to mind is the *canny edge* detection algorithm, which comes with the OpenCV package. Although this method is very good at detecting edges, the main limitation in this context is that it does not inherently distinguish between relevant edges (photo boundaries) and irrelevant ones (album background, shadows, or page structure).

An easer option seemed to be the use of ArUco markers.

#### Setup
