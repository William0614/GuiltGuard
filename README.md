# GuiltGuard
computer vision project that warns users when they attempt to consume unhealthy food.

## Aim:
Provide warning signs when a user attempts to consume beer or chocolate in front of camera.

## Development Process:
### 1. Create custom dataset on beer and chocolate.
  - Original Images: Total 126.
    - Chocolate 74 (Kitkat)
    - Beer 72 (Moretti)
  - Preprocessing: Auto-Orient, Stretch to 640x640
  - Augmentations:
    - Outputs per training example: 3
    - Flip: Horizontal, Vertical
    - 90° Rotate: Clockwise, Counter-Clockwise
    - Crop: 0% Minimum Zoom, 20% Maximum Zoom
    - Rotation: Between -15° and +15°
    - Shear: ±10° Horizontal, ±10° Vertical
    - Brightness: Between -15% and +15%
    - Blur: Up to 2.5px
    - Noise: Up to 0.1% of pixels

  - Total images: 308

### 2. YOLO11 object detection
  #### First Attempt: YOLO11m
   ![Screenshot 2025-02-17 at 6 02 46 PM](https://github.com/user-attachments/assets/b168db7f-3d85-4ae8-9f7a-c77bb06307d8)
     - Over spec to run on M1 sillicon CPU.
     - Too slow.
     - Inefficient for small custom dataset.
  #### Second Attempt: YOLO11n

