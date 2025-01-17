# Invisibility Cloak Effect using OpenCV

This Python project uses OpenCV to create an invisibility cloak effect. The inspiration behind this project is the idea of Harry Potter's invisibility cloak, where a person or object becomes invisible when they wear it. In this implementation, a specific color (blue) is made invisible using background subtraction and color filtering techniques.

The program captures video frames from the webcam and removes objects of a particular color (blue in this case) to simulate the invisibility effect. The program then blends the background with the "invisible" part, making the blue object disappear, just like an invisibility cloak.

## Features:
- **Background capture:** The program captures a series of frames to determine the background and use it for compositing when the blue color is removed.
- **Color filtering:** The program uses HSV color space to create a mask for the blue color, which is then used to remove or replace that color from the frame.
- **Cloak effect:** The program applies the cloak effect by blending the background where the blue color is detected.
- **Real-time processing:** The program runs in real-time and displays the result on your screen.

## Requirements:
- Python 3.x
- OpenCV
- Numpy

You can install the required libraries using the following command:

```bash
pip install opencv-python numpy
```

### Installation:

To get started, clone the repository and install the dependencies:

```bash
git clone https://github.com/yourusername/invisibility-cloak-opencv.git
cd invisibility-cloak-opencv
pip install -r requirements.txt
```
Or install the necessary libraries individually:
```bash
pip install opencv-python numpy
```

### Usage:
1. Run the script:
    ```bash
    python invisibility_cloak.py
    ```
2. Point a blue object in front of your webcam to see the invisibility effect.
3. Press 'q' to exit the program.    

### Code Explanation:
1. create_background(cap, num_frames=30): Captures the background using a series of frames to create a stable background.
2. create_mask(frame, lower_color, upper_color): Generates a binary mask for the color blue in the given frame.
3. apply_cloak_effect(frame, mask, background): Applies the invisibility cloak effect by blending the background where the blue color is detected.
4. main(): Main function to initialize the webcam, capture the background, and continuously apply the cloak effect.
