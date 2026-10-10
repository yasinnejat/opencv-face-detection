# Face and Eye Detection with OpenCV

A Jupyter Notebook that captures frames from a webcam and detects faces and eyes with OpenCV **Haar cascade** classifiers, first on a single frame and then in real time.

## Files
- `opencv_face_detection.ipynb` — the Jupyter Notebook.
- `requirements.txt` — Python dependencies.

## Before you run it
- The notebook needs a **webcam** (it opens camera `0`) and a desktop environment, because `cv2.imshow` opens a window. Run it on your own computer, not in a headless environment.
- Nothing is saved: frames are processed in memory only.
- The notebook uses `%matplotlib widget`, which requires the `ipympl` package (included in `requirements.txt`).

## Run the project
1. Install Python 3.10 or newer.
2. In this folder, install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open `opencv_face_detection.ipynb` in Jupyter Notebook, JupyterLab, or VS Code.
4. Run the cells from top to bottom. In the real-time cell, press `q` in the video window to stop.

## Workflow
1. Open the webcam with `cv2.VideoCapture` and read a frame.
2. Define a helper that shows an image in an OpenCV window.
3. Load the pre-trained Haar cascade models for faces and eyes that ship with OpenCV.
4. Convert the frame to grayscale.
5. Detect faces and eyes with `detectMultiScale`.
6. Draw rectangles around the detections.
7. Repeat the detection on live webcam frames and display the result in real time.
8. Crop the detected face region from the grayscale image.

## Limitations
- The single-frame cells assume exactly one face and two detected eyes in the frame.
- Haar cascades are fast but sensitive to lighting and head pose, and they can produce false detections.

## Technologies
Python, OpenCV, Haar Cascade Classifiers, Matplotlib, Jupyter Notebook.
