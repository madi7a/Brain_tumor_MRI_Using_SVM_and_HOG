# Brain Tumor MRI Classification Using SVM & HOG  

## 📌 Project Overview  
This project focuses on **classifying brain tumors from MRI images** using **Support Vector Machines (SVM) with Histogram of Oriented Gradients (HOG) feature extraction**. Additionally, a **GUI application** built with PyQt5 allows users to upload MRI scans and receive real-time predictions.  

## 📂 Dataset  
- **Source**: [Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)  
- **Classes Used**:  
  - **No Tumor**  
  - **Meningioma**  
- The model was tested on **all tumor types** in the dataset, including Glioma and Pituitary tumors.  

## 🛠️ Technologies Used  
- **Machine Learning**: Support Vector Machines (SVM)  
- **Feature Extraction**: Histogram of Oriented Gradients (HOG)  
- **Preprocessing**: OpenCV (image enhancement & cropping)  
- **GUI Development**: PyQt5 (interactive MRI classification app)  

## 🧹 Preprocessing Steps  
*Preprocessing code was adapted from a Kaggle notebook associated with the dataset.*  
- Convert MRI images to **grayscale** and apply **Gaussian blur**  
- Use **thresholding & morphological operations** to remove noise  
- Perform **contour detection** to focus on the tumor region  
- **Resize images** to ensure uniform input for the model  

## 🔬 Model Performance  
To find the best SVM kernel, I tested **Sigmoid, RBF, Polynomial (degree 2 & 3), and Linear kernels**.  

| Kernel  | Training Acc | Cross-Validation Acc | Validation Acc | Test Acc |
|---------|------------|----------------------|--------------|---------|
| Sigmoid | 90.37%    | 95.95%               | 96.25%       | 98.31%  |
| RBF     | 99.31%    | 95.78%               | 96.08%       | 96.62%  |
| Poly (2)| 99.95%    | 96.38%               | 96.59%       | 98.03%  |
| Poly (3)| 100%      | 96.29%               | 96.42%       | 98.17%  |
| Linear  | 100%      | 95.95%               | 96.25%       | 98.31%  |

✅ **Polynomial (degree 2) SVM provided the best balance of training and test accuracy.**  

## 🎮 GUI for Tumor Classification  
I developed an **interactive GUI using PyQt5** to make the model accessible.  
- Users can **upload an MRI image**  
- The model **predicts whether a tumor is present**  
- Simple **click-based interface** for easy use  

## 🚀 How to Run  
### 1️⃣ Install Dependencies  
Run the following command to install required packages:  
```bash
pip install -r requirements.txt
```  

### 2️⃣ Run the GUI  
Execute the following command to launch the MRI classification app:  
```bash
python gui.py
```  

## 📌 Key Takeaways  
✔ **Polynomial SVM (degree 2) performed best (Test Acc: 98.03%)**  
✔ **GUI application enhances usability for non-technical users**  
✔ **Preprocessing helped improve model robustness**  

This project showcases the power of **machine learning in medical imaging** and makes tumor classification more accessible! 🚀  
