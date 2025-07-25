# Face-Recognition-System-
Project Title: Face Recognition-Based Attendance System
Overview:
This project automates the attendance process using facial recognition technology. Instead of manually marking attendance, the system captures student images via webcam, identifies them by matching with a pre-trained database, and logs their attendance into a CSV file.



Key Features:
Face Recognition with Machine Learning:
Utilizes a Linear Support Vector Machine (SVM) classifier.
Employs Histogram of Oriented Gradients (HOG) for face encoding.
Extracts 128 facial measurements to identify individuals.




Real-time Face Detection via Webcam:
Captures live video feed using OpenCV.
Detects and compares live faces with stored images in the Students folder.

->Automatic Attendance Logging:
Matches recognized faces and logs the name with the current time into Attendance.csv.
Prevents duplicate entries for the same day.





File Structure:
Attendance.py: Main script that performs live face recognition and updates the attendance file.
Attendance.csv: Stores attendance records (Name, Time).
Students/: Folder containing labeled images of registered students.
README.md: Documentation and explanation of project workflow.



->How It Works:
*Training Phase:
Loads reference images from the Students folder.
Encodes each face using HOG.
Builds a face encoding dataset for comparison.

*Recognition Phase:
Uses the webcam to capture live faces.
Compares each detected face with the trained encodings.
If a match is found, updates the attendance in the CSV file with a timestamp.

*Verification:

Matching is based on Euclidean distance between the face encodings.
A threshold is used to ensure accuracy.

Technologies Used:
Python
OpenCV (for real-time video capture and image processing)
face_recognition library (for facial feature encoding and matching)
pandas (for handling the attendance CSV)
SVM (for face classification)

