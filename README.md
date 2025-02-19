# Sign Language Detection using Deep Learning

## Project Overview
This project focuses on real-time sign language detection using deep learning. It has two versions:
- **V1 (CNN-based)**: Uses a Convolutional Neural Network (CNN) trained directly on images without annotations.
- **V2 (MobileNetV2-based)**: Utilizes transfer learning with MobileNetV2 and a heuristic-based decision system for better accuracy.

The model takes input from a webcam, predicts the sign being performed, and matches it to a predefined dictionary of words.

---

## File Descriptions

### **V2Dataset Creation.ipynb**
This notebook is responsible for dataset creation. It:
- Creates **24 folders**, one for each sign label.
- Captures images from a **camera**, with a signer performing each sign.
- Saves images in their respective label folders using **OpenCV**.
- Ensures images are **uniquely named** to avoid overwriting.

### **V2realtime.ipynb**
This is the improved model for real-time sign detection. It:
- Loads a **pre-trained MobileNetV2 model** using TensorFlow.
- Uses **transfer learning** to fine-tune on the sign language dataset.
- Predicts sign labels in real-time using webcam input.
- Applies a **heuristic filtering system** to stabilize predictions.
- Matches predictions to a **dictionary of valid words** to ensure meaningful output.

### **V1 Real-time.ipynb**
The initial version that used a **CNN directly on raw images** for classification without annotations. It lacked heuristics and dictionary-based refinement.
