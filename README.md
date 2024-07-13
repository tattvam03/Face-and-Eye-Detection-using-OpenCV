# Face and Eye Detection using OpenCV
This project demonstrates a real-time face and eye detection system using OpenCV's Haar Cascade classifiers. The system captures live video from a webcam, processes each frame to detect faces and eyes, and visually marks the detected features.

### Features 
- Initialization:
  - The Haar Cascade classifiers for face and eye detection are loaded using cv2.CascadeClassifier.
- Video Capture:
  - A video capture object is created to access the webcam using cv2.VideoCapture(0).
- Frame-by-Frame Processing:
  - Each frame captured from the webcam is converted to grayscale using cv2.cvtColor.
  - The grayscale frame is scanned for faces using the face classifier (detectMultiScale method).
  - For each detected face, a bounding rectangle is drawn on the original frame.
  - The region of interest (ROI) for the face is extracted and scanned for eyes using the eye classifier.
  - Bounding rectangles are drawn around detected eyes within each face ROI.
- Display:
  - The processed frame with annotations is displayed in a window named 'Face and Eye Detection'.
  - The detection loop continues until the 'q' key is pressed.
- Cleanup:
  - The video capture object is released and all OpenCV windows are closed using cv2.destroyAllWindows().
