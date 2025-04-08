# Camera-Calibration & Lens Distortion Correction 
This is a camera calibration and lens distortion correction project using openCV python.

## Project Description

This project demonstrates how to calibrate a camera using a chessboard pattern and correct lens distortion in recorded video footage. It is implemented in Python with OpenCV, and follows a structured computer vision workflow to generate accurate camera intrinsic parameters and apply geometric correction.

## Dependencies
- Python 3.x
- OpenCV (opencv-python)
- NumPy

## Install
    pip install opencv-python numpy

## Chessboard Pattern Details

- **Printed Size**: A4
- **Square size**: 30 mm
- **Pattern used**: 9x7 squares → 8x6 **inner corners**
- **Video name**: `chessboard.avi`

---

##  Camera Calibration

Performed using OpenCV's `cv2.findChessboardCorners` and `cv2.calibrateCamera`.

<img width="544" alt="cv03 detection_image" src="https://github.com/user-attachments/assets/ecfaff47-cb3a-44aa-b1fe-86c572d944ff" />

- **RMS re-projection error**: **2.8746**
- **Camera Matrix (K)**: [[1543.4757 0. 981.8694 ] [ 0. 1538.5658 508.0066 ] [ 0. 0. 1. ]]
- **Distortion Coefficients (k1, k2, p1, p2, k3)**: [ 0.0268641, 0.2514341, -0.0003301, 0.0084674, -0.7652586 ]

---

##  Lens Distortion Correction

Performed using OpenCV’s `cv2.initUndistortRectifyMap` and `cv2.remap`.

- **Input video**: `chessboard.avi`
- **Corrected output**: `chessboard_corrected.avi`
 
<img width="1552" alt="cv03 lens_correction_image" src="https://github.com/user-attachments/assets/241e39ac-e7be-4e73-989a-c0a06b9340d3" />

---

## File Structure

    cv-assignments/
    ├── cv03.camera.py                # Calibrate camera from chessboard video
    ├── cv03.LENSdc.py                # Apply distortion correction to video
    ├── chessboard.avi                # Record chessboard video usind smartphone 
    ├── chessboard_corrected.avi      # Output corrected video
    └── README.md                     # Project documentation

---
## License

This project is licensed under the MIT License.

