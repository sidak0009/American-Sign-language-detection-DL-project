UEC642
DEEP LEARNING AND APPLICATIONS
American Sign Language Detection 

Submitted to:
Dr. Gaganpreet Kaur
Aug-Dec 2025

Submitted By:

Ishmit Singh-102215056
Adamya Sharma-102215132
Sumedha Khosla-102395002 

Introduction:
American Sign Language (ASL) is one of the most widely used communication systems among individuals with hearing or speech impairments. Traditional ASL interpretation requires human experts, which limits accessibility and makes real-time communication challenging. 
With recent advancements in artificial intelligence and computer vision, technology now offers new opportunities to support more accessible communication. Modern systems are increasingly capable of understanding visual cues, recognising patterns, and interpreting human gestures with greater accuracy and speed.
This project explores the development of an intelligent system that can identify hand gestures associated with the ASL alphabet. By combining deep learning techniques with real-time visual processing, the system aims to provide a flexible foundation for gesture-based communication tools. Such solutions have the potential to enhance accessibility, support inclusive interaction, and serve as a stepping stone toward more advanced sign-language recognition applications in the future.

Dataset:
For this project, we used the ASL Alphabet Dataset from Kaggle:
https://www.kaggle.com/datasets/grassknoted/asl-alphabet
The dataset contains images representing hand signs used in the American Sign Language (ASL) alphabet. Each image corresponds to one gesture and belongs to one of the ASL alphabet classes. The dataset is designed to support sign-language recognition systems and includes a diverse set of hand poses under different lighting and backgrounds.
The target class corresponds to the ASL letter being shown in the image, making this a multi-class classification task.

Target variable:
•	label: Indicates which ASL letter (A–Z) or special class (SPACE, NOTHING, DELETE) the image represents. Thus, the problem contains 29 distinct classes.
Dataset Size:
•	Total classes: 29
•	Images per class: ~3,000
•	Total images: ~87,000
•	Original Columns: 1 (Image)
•	Problem Type: Multi-class Classification

 
LITERATURE SURVEY:
Looking at previous work helped us decide the practical trade-offs for the product. We favoured lightweight, real-time-friendly tools like MediaPipe for landmark extraction, examined CNN/RNN/Transformer approaches, and chose a model family that supports continuous, sentence-level recognition rather than only isolated signs. The literature also made clear that public ASL datasets are limited, which motivated us to build a focused ASL alphabet/digits dataset.

The development of real-time communication systems for deaf-mute and hearing individuals has gained significant attention in recent years. Various research efforts have focused on improving sign language recognition, speech-to-sign translation, and bidirectional communication between users. This literature review examines key studies on sign language recognition, machine learning techniques, and speech-based captioning for sign conversion. By analysing existing methodologies, datasets, and research gaps, we aim to identify areas for further enhancement and innovation in this domain.  
Table 1 presents various state-of-the-art technologies for sign-to-text recognition, highlighting different approaches to converting sign language gestures into text. Techniques include k-NN for static gestures, HMMs for dynamic gestures, and CNN-based models such as CNN-DSC. MediaPipe is widely used for feature extraction, while LSTM aids in sequence classification. Despite advancements, challenges remain, such as sensitivity to lighting, lack of support for two-handed gestures, and limited standardised ASL datasets. Addressing these gaps can enhance system accuracy and usability.
Table 2 summarises various case studies evaluating sign language recognition and conversion techniques. Research explores deep learning architectures like CNNs, RNNs, and hybrid models, emphasising dataset diversity and benchmarking CSLR techniques. Key challenges include real-time processing, dataset limitations, and the need for more generalised models. Addressing these gaps can improve the inclusivity and efficiency of sign language translation systems.
 <img width="1151" height="638" alt="image" src="https://github.com/user-attachments/assets/b01a377a-61f0-46e2-a7a1-72a7be2f90fa" />
 <img width="1129" height="549" alt="image" src="https://github.com/user-attachments/assets/1f86b1e1-c416-4587-971d-c7a7dd9be062" />


Table 1. Comparison of various Sign-to-Text Recognition Techniques
Title	Method Used	Research Gap	Dataset	Results
Real-time ASL recognition (2018).	k-NN for static gestures, HMM for dynamic gestures	Sensitivity to lighting, no support for two-handed gestures	24,624 images of ASL digits, letters, and gestures, captured using a smartphone camera.	High accuracy (99.7% static, 97.23% dynamic)
Recognition of Indian Sign Language using Deep Learning Models (2022).	CNN with Depth-wise Separable Convolution (CNN-DSC)	Lack of a standardised ASL dataset	Dataset, including a self-collected dataset with 65 users and a publicly available dataset.	Efficient two-handed gesture recognition, 92.43% accuracy
Automatic Indian Sign Language Recognition using MediaPipe Holistic and LSTM Network (2023).	MediaPipe Holistic for feature extraction, LSTM for classification	Inter-class similarities, dataset inconsistencies	Include the dataset.	Achieves 94.8% accuracy, extracts 3D skeletal key points
Understanding vision-based continuous sign language recognition (2020).	Analysis of CSLR models (HMMs, DTW, CNNs, LSTMs, Transformers)	Real-time processing and occlusion handling remain challenges	RWTH- Phoenix- weather, SIGNUM, Synthetic Vocab.	Focus on robust feature extraction and temporal modelling
Sign Language Recognition and Translation Systems for Enhanced Communication for the Hearing Impaired (2024).	Integration of SLR with ASR, CNNs, LSTMs, and Transformers	Lacks bidirectional communication	Robita ASL and Own dataset created by taking webcam images.	Enhances accuracy, enables gesture-based communication
Real-time SIGN Recognition System to aid deaf-dumb people (2011).	Machine Learning (Simple Threshold Values)	Limited Gesture Set	320 images.	Achieved 98.125% accuracy in real-time recognition when tested on 160 images.
Automatic ASL recognition system (2013).	Image processing, HU-invariant moments, SVM	Limited to controlled environments, no dynamic gestures.	The dataset contains 720 images created in-house.	96.23% accuracy for static gestures
Sign Language Translation Across Multiple Languages (2024).	SVM, CNN, 3D-CNN	No detailed implementation provided	Dataset of 35,000 images.	High accuracy for colour (99.72%) and grayscale (99.90%) images

Table 2. Case Studies for Sign Language Recognition
Title	Method Used	Research Gap	Dataset	Result
Sign Language Recognition: A Deep Survey (2021).	Survey on CNNs, RNNs, hybrid models	Dataset diversity, model robustness, and continuous sign recognition	Multi-Lingual datasets used	Comprehensive analysis of deep learning models
Reviewing 25 years of continuous sign language recognition research: Advances, challenges, and prospects. (2024) 	Review of CSLR techniques (HMMs, CNNs, RNNs)	No new methods proposed	Multi-Lingual datasets used	Highlights the importance of large datasets
 
RESEARCH GAPS
•	Dependence on Human Interpreters: Expensive and not always available during spontaneous or emergency interactions.
•	Low Accuracy for Complex Signing: Difficulty recognising dynamic or fast signing styles.
•	Standalone Gesture Apps: Existing apps only handle basic gestures; they struggle with real-time, fluid signing.
•	One-Way Translation Tools: Tools like speech-to-text only offer one-directional communication, failing to support inclusive interaction.
•	Wearable-Based Solutions: Gloves and sensor-based systems are costly, bulky, and impractical for daily use.
•	Latency and Responsiveness Issues: Many tools show delay and poor real-time response, impacting usability in critical contexts like education or healthcare.
•	Limited Support for Continuous Signing: Most systems can't handle ongoing sign language streams or multilingual gestures effectively.
•	High Infrastructure Cost: Existing solutions often require expensive hardware or professionally trained staff, reducing accessibility.
•	Lack of Unified, Open-Source Systems: Existing solutions handling sign are commercially licensed or complex to use, and lack real-time, offline, multi-input support accessible to the deaf and speech-impaired.

Methodology:
This project follows a structured pipeline to build an ASL alphabet recognition system capable of performing real-time gesture classification. The process involves dataset preparation, feature extraction using hand landmarks, model training using deep learning (MLP classifier), and finally, real-time prediction using webcam input. The major steps are described below.
 <img width="445" height="734" alt="image" src="https://github.com/user-attachments/assets/c789e0c3-f24a-4084-b091-8a40e6ea68a6" />
 <img width="334" height="732" alt="image" src="https://github.com/user-attachments/assets/3e50d61a-ed74-4630-982a-8fe6c8a29766" />
 <img width="256" height="262" alt="image" src="https://github.com/user-attachments/assets/da7d8427-24e7-4fd2-8a48-6f83d7c0b155" />

1. Dataset Loading
The ASL Alphabet dataset was imported from Kaggle, containing image folders for 29 classes (A–Z, SPACE, DELETE, NOTHING). Using Python, the dataset directory was scanned, and all image files were collected class-wise. Each folder name served as the class label.
Initial inspection included:
•	Counting images per class
•	Checking directory structure
•	Verifying valid image formats (.jpg, .png, .jpeg)

2. Hand Landmark Extraction Using MediaPipe
Before training any model, every image requires preprocessing and structured feature extraction.
a) Using MediaPipe Hands: Google’s MediaPipe Hands model was used to detect a single hand and extract 21 key landmarks per image.
b) Converting Images to Landmark-Based Features:
For each image:
•	The hand was detected
•	21 landmarks (x, y, z) were extracted
•	Wrist point (landmark 0) was used as a reference
•	All landmarks were normalised by subtracting wrist coordinates
(to reduce variation in hand position and camera distance)
If no hand was detected, the image was marked as failed and excluded.
Each sample was finally represented as:
•	63 numerical features (21 landmarks × 3 coordinates)
This approach reduces noise and captures the geometric structure of the ASL gesture more efficiently than raw images.

3. Dataset Construction
All extracted landmarks were combined into a Pandas DataFrame with:
•	63 landmark features
•	1 target label (class name)

Column format:
label, x0, y0, z0, x1, y1, z1, ... , x20, y20, z20
The dataset was then saved in pickle format (asl_landmarks.pkl) for model training.

4. Label Encoding
Since the target variable (label) consisted of strings (A, B, C, …),
LabelEncoder was used to convert each class into an integer:
•	Example: A → 0, B → 1, C → 2, etc.
This numeric encoding is required for training deep learning models.

5. Train-Test Split
The dataset was split into:
•	80% training data
•	20% testing data
Stratification ensured that each class had proportional representation in both splits.

6. Feature Scaling
Because neural networks perform better when input features are normalised,
StandardScaler was applied:
•	fit_transform() applied to training data
•	transform() applied to test data
This standardised all 63 features to have a mean of 0 and a variance of 1.

7. Model Building Using MLP Classifier
The classification model used in this project is a Multilayer Perceptron (MLP) built with TensorFlow/Keras.
Key components included:
•	Dense layers: 256 → 128 → 64 neurons
•	ReLU activation for non-linearity
•	Batch Normalization for stable training
•	Dropout to reduce overfitting
•	Softmax output layer for multi-class classification (29 classes)
The model was compiled using:
•	Adam optimizer (learning rate = 0.001)
•	sparse_categorical_crossentropy loss
•	Accuracy as evaluation metric
Callbacks such as EarlyStopping, ReduceLROnPlateau, and ModelCheckpoint were used to improve performance.

8. Model Training
The network was trained for up to 100 epochs with:
•	Batch size = 128
•	Validation on the test set
•	Automatic learning-rate reduction when validation loss plateaued
The best-performing model (highest validation accuracy) was saved.

9. Model Prediction and Evaluation
After training, the best model was evaluated on the test data.
Metrics calculated:
•	Accuracy (overall correctness)
•	Loss (model error)
•	Confusion Matrix – showing correct vs incorrect predictions per class
•	Classification Report – precision, recall, F1-score for each of the 29 classes
Training and validation curves for accuracy and loss were plotted to assess learning behaviour.

10. Saving the Final Components
Three essential files were saved for real-time inference:
1.	asl_model.h5 – trained MLP model
2.	scaler.pkl – feature scaler
3.	label_encoder.pkl – encoded class mapping
These files were required to deploy the model for live webcam-based recognition.

11. Real-Time Gesture Detection
For real-time prediction:
•	Webcam frames were captured using OpenCV
•	MediaPipe extracted hand landmarks on each frame
•	Landmarks were normalised and scaled using the saved scaler
•	The trained model predicted the ASL class
•	Prediction was displayed live on the video feed
This completed the end-to-end ASL recognition system using deep learning and computer vision.

Results:
After training the deep learning–based ASL classification model on the extracted hand-landmark features, the model was evaluated on the unseen 20% test split. Multiple performance metrics were calculated to assess how accurately the system can recognise ASL alphabet signs.

• Accuracy:
•	Training Accuracy: 99.78%
•	Testing Accuracy: 99.53%
This indicates that the model performs extremely well on both training and unseen data. With a test accuracy of 99.53%, the classifier correctly identifies approximately 995 out of every 1000 ASL gestures, demonstrating excellent generalisation.

• Loss Values:
•	Training Loss: 0.0064
•	Testing Loss: 0.0223
Very low loss values indicate that the neural network has learned the gesture representations effectively, and no major overfitting is observed due to regularisation techniques such as dropout and batch normalisation.

• Classification Report:
A detailed classification report was generated for all 29 classes (A–Z, del, space, nothing), including precision, recall, and F1-score for each class.
 <img width="917" height="980" alt="image" src="https://github.com/user-attachments/assets/ccebee31-0021-463e-9f17-9baf624220c2" />
 <img width="945" height="706" alt="image" src="https://github.com/user-attachments/assets/048cc8b3-fd22-4b48-a9cd-8644c000edcb" />

This confirms the model’s strong ability to correctly detect each ASL sign with very minimal misclassification.
Only a few gestures (e.g., M and N) show slightly lower scores due to high visual similarity in their hand shapes.

• Confusion Matrix:
The confusion matrix shows that the model makes very few mistakes across all sign categories. Most entries lie on the diagonal, confirming that the predicted class usually matches the true class.
Misclassifications — where present — occur between visually similar signs, which is expected due to close resemblance in hand-pose geometry.
 <img width="945" height="756" alt="image" src="https://github.com/user-attachments/assets/69f0e360-d4c2-4acc-9f18-f702a8176eae" />


• Training Curves:
Training curves for accuracy and loss indicate:
•	Rapid improvement during early epochs
•	Stable convergence
•	Narrow gap between training and validation curves
•	No significant overfitting
The model’s learning behaviour remains consistent and reliable across the entire training process.
 <img width="945" height="315" alt="image" src="https://github.com/user-attachments/assets/7a719e5e-4fa4-4a42-ac92-a8c8528dba3a" />

•	Real-Time Performance:
In addition to offline evaluation, the model was integrated into a live webcam-based ASL recognition system using OpenCV and MediaPipe.
<img width="945" height="728" alt="image" src="https://github.com/user-attachments/assets/627478aa-888d-4434-bc31-2ce104b105c6" />
<img width="933" height="677" alt="image" src="https://github.com/user-attachments/assets/7c69bc0e-7da6-4731-a340-85318c1b0f5a" />
<img width="945" height="757" alt="image" src="https://github.com/user-attachments/assets/1061ad0f-3207-48ab-a09f-ab8438652e1b" />

Conclusion: 
This project successfully demonstrated how deep learning and computer vision can be used to recognise American Sign Language (ASL) gestures with high accuracy. By using the ASL Alphabet dataset from Kaggle and extracting 3D hand landmarks through MediaPipe, the system transformed raw images into structured numerical features suitable for machine-learning models. A Multilayer Perceptron (MLP) classifier was then trained on these features to learn the hand-pose patterns corresponding to different ASL letters.
The final model achieved outstanding performance, including:
•	99.53% test accuracy
•	Extremely low loss values
•	High precision, recall, and F1-scores across all 29 gesture classes
•	A confusion matrix indicating very few misclassifications
These results clearly show that a landmark-based deep learning approach is highly effective for ASL alphabet recognition. The combination of MediaPipe’s robust hand-tracking and the neural network's ability to learn gesture variations enables reliable and efficient gesture classification.
Beyond training, the model was successfully integrated into a real-time detection pipeline using a webcam, allowing live sign recognition frame by frame. This demonstrates the practical potential of the project in real-world applications such as assistive communication tools, educational platforms, or gesture-controlled systems.
Overall, this project highlights how AI-driven techniques can make sign-language recognition more accessible, accurate, and scalable. It serves as a strong foundation for future work, including full-word recognition, sentence-level interpretation, and deployment on mobile or embedded devices.










































