### **Real-Time Drowsiness Detection System**  

#### **Overview**  
This system detects driver drowsiness in real-time using computer vision and alerts the user with an alarm. It captures live video, analyzes facial and eye landmarks, and detects prolonged eye closure to determine drowsiness.  

#### **Motivation**  
Drowsy driving causes thousands of accidents yearly. This project aims to reduce such incidents by providing an automated alert system.  

#### **Technologies Used**  
- **OpenCV** – Image processing and face detection  
- **imutils** – Simplifies OpenCV functions  
- **Dlib** – Facial landmark detection  
- **Scikit-learn** – Machine learning for analysis  
- **NumPy** – Scientific computing  

#### **Setup & Installation**  
1. **Install Python 3** and **CMake**  
2. **Clone the repository**:  
   ```sh
   git clone <repository-link>
   cd Real-Time-Drowsiness-Detection-System
   ```  
3. **(Optional) Create a virtual environment**:  
   ```sh
   pip install virtualenv  
   virtualenv -p python3 test_env  
   test_env\Scripts\Activate  # Windows  
   source test_env/bin/activate  # Unix  
   ```  
4. **Install dependencies**:  
   ```sh
   pip install -r requirements.txt  
   ```  
5. **Run the application**:  
   ```sh
   python Real-Time-Drowsiness-Detection-System.py --shape-predictor shape_predictor_68_face_landmarks.dat --alarm Alert.wav  
   ```  

#### **Algorithm Steps**  
1. Capture the driver’s face using a camera.  
2. Detect the face using Haar cascades.  
3. If the face is missing, trigger an alert.  
4. Detect eyes and check if both are visible.  
5. Analyze eye state using pupil detection.  
6. If eyes remain closed for five consecutive frames, trigger an alert.  

#### **Testing & Results**  
The system was tested under different conditions, including:  
- Varying lighting  
- Different face positions (center, left, right)  
- Wearing spectacles  
- Head tilting beyond 30 degrees reduced detection accuracy  

#### **Future Scope**  
- **Smartphone Application** – Can be integrated into a mobile app for wider accessibility.  

This system effectively detects driver drowsiness and can be further enhanced for real-world applications. 🚗💡
