# Gender Prediction from Image Using DeepFace (Computer Vision)

This project predicts **gender** from a single image using the **DeepFace** library. It loads an input image, runs DeepFace analysis for gender detection, prints the predicted gender, and displays the image with the prediction label.

ML flow covered: **Problem Statement → Selection of Data → Collection of Data → Preprocessing → Model/Library Selection → Output**

---

## Problem Statement

Given a person’s face image, predict the **dominant gender** using a pre-trained deep learning model.

**Output:** Predicted gender label (example: `Man` / `Woman`)

---

## Selection of Data

**Dataset Type Used:** Face image (single image input)

The model expects a clear face image (front/near-front face works best).

---

## Collection of Data

This project uses:
- An input image uploaded into the runtime: `person.jpg`
- Gender detection is performed using DeepFace’s pre-trained models

---

## Preprocessing

Basic preprocessing in this project:
- Read image using OpenCV: `cv2.imread()`
- Convert BGR to RGB before displaying using Matplotlib:
  - `cv2.cvtColor(img, cv2.COLOR_BGR2RGB)`

Note:
- `enforce_detection=False` allows running even if face detection is weak (useful for learning/demo).

---

## Model / Library Selection

**Library used:** `DeepFace`

Used function:
- `DeepFace.analyze(img_path=IMAGE_NAME, actions=["gender"], enforce_detection=False)`

DeepFace returns analysis results, and this project extracts:
- `dominant_gender`

---

## Evaluation / Output

This project outputs:
- Printed predicted gender:
  - `Predicted Gender: <gender>`
- Displays the image with title:
  - `Predicted Gender: <gender>`

---

## Main Libraries Used (and why)

1. `deepface`  
   - Performs pre-trained gender analysis from face image.

2. `opencv-python (cv2)`  
   - Loads image and converts color space for display.

3. `matplotlib`  
   - Displays the input image with predicted gender label.

---

## How to Run (Colab)

### Step 1: Install dependencies
```bash
!pip install deepface opencv-python matplotlib
```

### Step 2: Upload the image
- Upload an image named `person.jpg` (or change `IMAGE_NAME` in the code)

### Step 3: Run the code cells
- DeepFace analyzes the image  
- Gender is printed and shown on the image  

---

## Output
- Predicted gender printed in the output cell  
- Image displayed with the predicted gender label  

---

## Developer
Grishma C.D
