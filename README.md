# 🧠 Brain Tumor Detection using CNN

This project uses a Convolutional Neural Network (CNN) to detect brain tumors from MRI images. The model is trained and tested entirely within a single Jupyter Notebook.

## 📘 Project Highlights

- Built with TensorFlow and OpenCV
- Dataset structured into `yes/` and `no/` folders (tumor / no tumor)
- Uses image preprocessing like brain contour cropping
- Works on local image files (no external Drive needed)
- No need to rename files with spaces — handled dynamically

## 📁 Folder Structure

brain-tumor-project/
│
├── brain_tumor_detector.ipynb # Main notebook with training & prediction
├── yes/ # MRI images with tumors
└── no/ # MRI images without tumors

markdown
Copy
Edit

## 🧪 How It Works

1. **Image Preprocessing**:
   - Each image is read using OpenCV.
   - Brain region is extracted using contour detection.

2. **Model Architecture**:
   - A CNN is trained on 240x240 MRI images.
   - Model outputs a binary classification (tumor / no tumor).

3. **Prediction**:
   - You can test with any image from `yes/` or `no/` folder.
   - Output example:  
     ```
     ✅ The MRI image has a Tumor
     ```

## 🖼️ Sample Image Loading (Auto-handles Spaces)

```python
import os, cv2

images = os.listdir("no")
img_path = os.path.join("no", images[0])
img = cv2.imread(img_path)
✅ No need to rename images with spaces!

🧠 Example Output
Prediction: ✅ The MRI image has a Tumor


🔗 Run in Google Colab
[
]
(https://colab.research.google.com/github/Praneeth1636/brain-tumor-project/blob/main/brain_tumor_detector.ipynb)

✍️ Author
Praneeth Yashovardhan Kadem

📜 License
This project is open-source and free to use for educational purposes.

yaml
Copy
Edit

---

### ✅ Next Step:
Save that as `README.md` in your project folder, then run:

```bash
git add README.md
git commit -m "Added detailed project README"
git push
