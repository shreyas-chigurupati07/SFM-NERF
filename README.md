# Building built in minutes- SfM and NeRF

## Project Overview

This project focuses on reconstructing a building's 3D structure from different views using various computer vision techniques and synthesizing novel views of complex scenes using Neural Radiance Fields (NeRF).

## Key Components

1. **Structure from Motion (SfM):** Utilizes epipolar geometry, Non-linear Triangulation, Perspective N Points, and Bundle Adjustment to reconstruct 3D structures from multiple images.
2. **Neural Radiance Fields (NeRF):** Implements Tiny NeRF to synthesize novel views of the scene, optimizing a continuous volumetric scene function with a limited number of input views.

## Implementation Details

- Dataset: Five images of Unity Hall at WPI, captured using a Samsung S22 Ultra, scaled to 800x600 pixels.
- Feature Extraction: Utilizes SIFT for robust feature detection and matching, refined by RANSAC to eliminate outliers.
- Fundamental and Essential Matrix Estimation: Employs the normalized 8-points algorithm to estimate matrices capturing the scene's intrinsic geometry.
- Camera Pose and Triangulation: Determines the camera pose and applies Linear and Non-Linear Triangulation methods for 3D point estimation.
- PnP and Bundle Adjustment: Perspective N Points (PnP) for estimating camera pose and Bundle Adjustment for refining 3D points and camera poses.
- NeRF Implementation: Tiny NeRF model trained to render 3D scenes from sparse 2D inputs, focusing on volume density and RGB color estimation.

## Results

The project successfully reconstructs the 3D structure of Unity Hall and synthesizes new views using the trained NeRF model, demonstrating the effectiveness of combining classical computer vision techniques with deep learning for scene reconstruction.


https://github.com/shreyas-chigurupati07/SFM-NERF/assets/84034817/7d7f4c1e-234a-4b4c-b847-eb38bb2116da


## How to Run

1. Clone the repository: `git clone [repository-link]`
2. Navigate to the project directory: `cd [project-directory]`
3. Execute the scripts for SfM and NeRF: `python sfm.py` and `python nerf.py`

## Dependencies

- Python
- NumPy
- Matplotlib
- SciPy
- PyTorch (for NeRF)


## References

- Ben Mildenhall et al., "NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis."

