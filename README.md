# Smart Fruit Freshness Detector with Real-Time Audio Feedback

### Overview
"Smart Fruit Freshness Detector with Real-Time Audio Feedback" is a machine learning project aimed at determining the freshness of fruits using a real-time camera feed. The model classifies fruits as either fresh or rotten and provides an audio response based on the classification. This project is useful for quick quality checks in various settings, such as supermarkets, warehouses, or even home kitchens.

### Features
- **Real-Time Classification:** Uses a camera to capture images of fruits and classify them on the spot.
- **Audio Feedback:** Provides immediate verbal feedback on the freshness of the fruit, aiding users who may not be able to interpret visual results.
- **Multi-Class Support:** Capable of handling multiple types of fruits, with separate classifications for fresh and rotten states.

### Dataset
The model was trained on a dataset containing images of various fruits, each labeled as "good" or "bad." The dataset includes multiple categories such as:
- Good Apple
- Bad Apple
- Good Banana
- Bad Banana
- Good Orange
- Bad Orange

### Model Architecture
The model used is a Convolutional Neural Network (CNN) with the following architecture:
- **Convolutional Layers:** Extract features from the input images.
- **Fully Connected Layers:** Classify the extracted features into the predefined classes.
- **Output Layer:** Provides probabilities for each class, helping to determine the fruit's condition.

### Training
- **Loss Function:** Cross-Entropy Loss, which is suitable for multi-class classification.
- **Optimizer:** Adam optimizer for efficient gradient descent.
- **Device Support:** Training can be done on both CPU and GPU (CUDA supported).

### Real-Time Processing
The model is deployed on a device with a connected camera. It captures frames in real-time and processes each frame to identify the fruit's condition:
1. The camera captures an image.
2. The image is passed through the trained model to predict the fruit's state.
3. If a fruit is classified as "fresh" and remains so across multiple frames, the audio output confirms, e.g., "Fresh Apple."
4. If any part of the fruit is classified as "rotten" in any frame, it gives an immediate audio output like "Rotten Apple."

### Audio Feedback
The project uses a text-to-speech engine to convert the classification results into audio feedback. This helps provide immediate and accessible results to the user without requiring visual confirmation.

### How to Use
1. **Load the Model:** The pre-trained model is loaded from a saved file (`fruit_classifier.pth`).
2. **Connect a Camera:** Ensure a camera is connected to capture real-time video feed.
3. **Run the Script:** Execute the script to start the real-time fruit classification process.
4. **Receive Feedback:** As the model processes the input from the camera, it will provide audio feedback indicating whether the fruit is fresh or rotten.

### Dependencies
- PyTorch
- OpenCV
- Pyttsx3 (for audio feedback)


### Future Improvements
- **Enhanced Dataset:** Include more fruit types and variations to improve model generalization.
- **Mobile Deployment:** Optimize the model for deployment on mobile devices for portability.
- **User Interface:** Develop a GUI to make it more user-friendly.

### Conclusion
This project demonstrates the application of deep learning for real-time object detection and classification, providing practical solutions with immediate feedback through audio. It can be an invaluable tool in various environments where quick quality checks of fruits are necessary.
