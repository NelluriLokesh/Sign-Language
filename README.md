# Sign Language Detection

## Overview
This project uses a trained deep learning model to recognize sign language gestures from images. The model is built using TensorFlow and Keras and predicts alphabetic signs (A-Z) based on input images from a test dataset.

## Prerequisites
Before running the script, ensure you have the following installed:
- Python 3.x
- TensorFlow
- NumPy
- Pandas
- OpenCV (optional for image preprocessing)

You can install the necessary dependencies using:
```bash
pip install tensorflow numpy pandas opencv-python
```

## Project Structure
```
Sign-Language-detection/
│── sign_language_model.h5  # Pretrained model file
│── testdatabase/           # Folder containing test images
│── script.py               # The main script for prediction
│── sign_language_predictions.csv  # Output file with predictions
```

## How to Use
1. Place the trained model (`sign_language_model.h5`) in the project directory.
2. Ensure test images are stored inside the `testdatabase` folder.
3. Run the script:
   ```bash
   python script.py
   ```
4. The script will generate predictions and save them in `sign_language_predictions.csv`.

## Code Explanation
- **Model Loading:** Loads the pre-trained model (`sign_language_model.h5`).
- **Data Preprocessing:** Uses `ImageDataGenerator` to rescale test images.
- **Prediction:** The model predicts the class (A-Z) for each test image.
- **Result Saving:** Saves the predictions to a CSV file.

## Output
After execution, the script generates a CSV file with predicted categories for each image:
```
filename          | Predicted_Category
--------------------------------------
image1.jpg       | A
image2.jpg       | B
...
```

## Notes
- Ensure the test image dimensions match the model's input size (128x128 pixels).
- The model should be trained beforehand on a dataset of sign language images.

## Future Improvements
- Improve model accuracy with more training data.
- Add real-time sign language detection using a webcam.
- Develop a GUI for easier interaction.

## License
This project is open-source and available for educational purposes.

## Author
Nelluri Lokesh
