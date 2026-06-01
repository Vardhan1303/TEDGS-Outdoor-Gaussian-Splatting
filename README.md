# TEDGS: Outdoor 3D Gaussian Splatting Reconstruction

Real-world outdoor scene reconstruction using COLMAP and
3D Gaussian Splatting from a custom smartphone-captured dataset.

## This project explores the complete 3D reconstruction pipeline:

1. Outdoor data acquisition
2. Structure-from-Motion using COLMAP
3. Camera pose estimation
4. 3D Gaussian Splatting training
5. Novel-view synthesis

The goal was to understand modern 3D vision pipelines from
data collection to neural rendering.

## Dataset was captured in an outdoor park using a smartphone.

Scene:
- Outdoor statue
- Natural lighting
- Circular camera trajectory

Images used:
- 75 images

Capture strategy:
- Full orbit around object
- Multiple viewing elevations

## Pipeline

Video
 ↓
Frame Extraction
 ↓
COLMAP
 ↓
Sparse Reconstruction
 ↓
Camera Poses
 ↓
3D Gaussian Splatting
 ↓
Novel View Synthesis

## Challenges encountered:

- Initial COLMAP reconstruction registered only 2 images.
- Excessive frame redundancy reduced matching quality.
- Outdoor vegetation introduced dynamic scene artifacts.
- Sequential matching significantly improved reconstruction.

### Sparse Reconstruction

[COLMAP image]

### Gaussian Splatting

3000 Iterations

[image]

7000 Iterations

[image]

10000 Iterations

[image]

## Key takeaways:

- Camera pose estimation quality strongly affects 3DGS results.
- Dataset quality is more important than increasing iterations.
- Sparse-view reconstruction remains challenging.
- Dynamic scene elements can introduce artifacts.

## ## Acknowledgements

This project builds upon:

- 3D Gaussian Splatting (Kerbl et al., 2023)
- COLMAP (Schönberger et al.)

Official repositories:

- Gaussian Splatting: [[link](https://github.com/graphdeco-inria/gaussian-splatting?utm_source=chatgpt.com)]
- COLMAP: [[link](https://github.com/colmap/colmap?utm_source=chatgpt.com)]
