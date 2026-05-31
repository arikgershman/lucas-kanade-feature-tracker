# Feature Tracker: Lucas-Kanade & Harris Corner Detection 🎯
* **Course:** CMSC426
* **Author:** Arik Gershman

## Viewing This Project
The Jupyter notebook contains embedded output and visualizations, which makes it too large to render directly on GitHub. For the best experience:
* 📄 **[View the PDF](CMSC426_Assignment2_sp26.pdf)** — recommended for a quick look at the code and results
* 📓 **[View the rendered HTML notebook](https://arikgershman.github.io/lucas-kanade-feature-tracker/CMSC426_Assignment2_sp26.html)** — for viewing the code and outputs
* 💾 Download the `.ipynb` file to run it locally

## Project Overview
This project implements a robust corner detector and feature tracker from scratch to track points of interest across an image sequence (the "hotel" dataset). The implementation relies on fundamental computer vision mathematical models rather than pre-existing tracking functions from libraries like OpenCV.

## Methodology
The pipeline is broken down into two main components:

**1. Keypoint Selection (Harris Corner Detection)**
* Approximates the Sum of Squared Differences (SSD) error using Taylor expansion.
* Constructs the structure tensor (H matrix) using image gradients (Ix, Iy).
* Applies the Harris operator to evaluate corner strength and uses non-maximum suppression to isolate the most prominent keypoints, filtering out flat regions and straight edges.

**2. Feature Tracking (Lucas-Kanade Algorithm)**
* Tracks the detected keypoints frame-by-frame through the image sequence.
* Utilizes optical flow principles to estimate the movement of the selected corners across subsequent images.

## Technologies Used
* **Language:** Python
* **Environment:** Jupyter Notebook
* **Libraries:** NumPy, SciPy (for interpolation and multi-dimensional image processing), Matplotlib, OpenCV (strictly for basic image I/O and color space conversions)
