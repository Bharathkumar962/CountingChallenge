# CountingChallenge

## Description

### AI
The AI solution utilizes the YOLOv5 model to detect and count items in an image. The model, loaded via torch.hub, is a pre-trained deep learning model capable of identifying objects and their bounding boxes. The image is processed by converting it to RGB format before passing it to the model for inference. The detected objects' bounding boxes and labels are drawn on the image, and the total count of items is determined. The result is saved as an output image and displayed using matplotlib.

#### YOLOv5 Implementation Steps:
1. **Set Up the Environment**: Install necessary libraries like torch, torchvision, numpy, opencv-python, and matplotlib.
2. **Download and Set Up YOLOv5**: Clone the YOLOv5 repository and install the required packages.
3. **Load the YOLOv5 Model**: Use torch.hub to load the pre-trained YOLOv5 model.
4. **Load and Process the Image**: Read the input image, convert it to RGB format, and pass it to the YOLOv5 model for object detection.
5. **Draw Bounding Boxes and Labels**: Draw bounding boxes and labels on the detected objects.
6. **Save and Display the Result**: Save the output image with detected items and display it using matplotlib.

The script `count_items_Ai.py` implements the above steps and counts the items in the image accurately.

### Non_AI
The non-AI solution employs OpenCV for image processing and item counting. The image is first converted to grayscale and then blurred to reduce noise. Adaptive thresholding is applied to create a binary image, followed by morphological operations to refine the binary mask. Contours of the items are detected and drawn on the original image. The total number of items is counted based on the detected contours. The processed image with contours is saved as the output image.

## Additional Comments
This project demonstrates the effectiveness of both AI and non-AI techniques in counting items in an image and overlaying masks. The AI method leverages the power of deep learning for accurate object detection, while the non-AI method showcases traditional image processing techniques. The inclusion of the YOLOv5 model highlights the advanced capabilities of modern AI solutions for complex image analysis tasks.