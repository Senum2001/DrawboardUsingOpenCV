# Drawboard using OpenCV and MediaPipe

## Libraries Used:
- **MediaPipe**: Used to build multimodal ML pipelines.
- **OpenCV**: Image and Video Processing.

## Hand Detection:
- Initializes MediaPipe's Hand solution with specified thresholds.
- Loads an image containing drawing tools (`tools.png`).
- Creates a white mask for drawing operations.

## Main:
- Opens the webcam, flips the frame, converts it to RGB, and processes each frame using MediaPipe to detect the hand.
- It draws the landmarks on the hand.
  - Checks if the hand is within the tool selection area and selects the tool based on the x-coordinate of the hand's index finger.
  - Depending on the selected tool, performs the corresponding drawing operation (line, rectangle, circle, free draw, or erase) on the mask.

- Combines the mask with the original frame to show the drawing effect.
- Displays the frame with the selected tool overlay.
- Exits the loop and releases resources if the `Esc` key is pressed.
