# Real-Time Motion Detection Using OpenCV

This project implements a basic real-time motion detection system using Python and OpenCV.
The goal is to detect meaningful motion in a video stream by comparing each frame with a
static background reference.

---

## Project Overview

- The first captured frame is used as a background reference.
- Each incoming frame is compared with the background to detect changes.
- Small, insignificant differences (noise) are filtered out.
- Detected motion regions are highlighted using bounding boxes.

This approach is commonly used as a foundation for surveillance systems and industrial
monitoring applications.

---

## Methodology

The motion detection pipeline consists of the following steps:

1. **Grayscale Conversion**
   - Frames are converted to grayscale to reduce computational complexity.

2. **Gaussian Blurring**
   - Applied to reduce noise and smooth small intensity variations.

3. **Background Subtraction**
   - Absolute difference between the background frame and the current frame.

4. **Thresholding**
   - Converts the difference image into a binary (black–white) motion mask.

5. **Morphological Dilation**
   - Expands detected regions to obtain continuous motion areas.

6. **Contour Detection and Filtering**
   - Contours with small areas are ignored to eliminate noise.
   - Valid motion regions are marked with bounding boxes.

---

## Technologies Used

- Python
- OpenCV (cv2)
- NumPy

---

## Example Output

- **Main Window:** Live camera feed with detected motion highlighted.
- **Threshold Window (Debug):** Binary mask showing motion regions.

---

## Notes

- The threshold visualization window is used for debugging and parameter tuning.
- Area filtering helps reduce false positives caused by lighting changes or camera noise.


