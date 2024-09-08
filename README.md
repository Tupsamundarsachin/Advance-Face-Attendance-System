# face-attendance-system
The Advanced Face Attendance System is an enhanced computer vision-based application that not only detects and recognizes faces for attendance logging but also includes an anti-spoofing feature. This feature ensures the system can differentiate between real-life persons and photographs or videos, enhancing security.
![Spoofing](https://github.com/user-attachments/assets/89a43614-271f-45f0-8956-7d2550856bfa)


## spoofing feature

After cloning the first repo https://github.com/Tupsamundarsachin/Advance-Face-Attendance-System.git you need to clone the silent-Face-Spoofing repo in your root repo that is in first repo
Github link to clone the silent-face-spoofing repo

    git clone https://github.com/Tupsamundarsachin/Silent-Face-Anti-Spoofing.git
    pip install -r Silent-Face-Anti-Spoofing/requirements.txt

Remember to add the Silent-Face-Anti-Spoofing directory to your **PYTHONPATH**.


## Features

10 Face Detection and Recognition: Identifies and authenticates users based on their facial features.
2) Anti-Spoofing: Detects and blocks attempts to fool the system using photos or videos.
3) Automatic Attendance Logging: Logs recognized users' attendance with timestamps.
4) New User Registration: Allows new users to register by capturing their facial data and storing it securely in the database.
5) Real-time Processing: Continuously processes live webcam feed for immediate recognition and feedback.


## Requirements
To run this project, you need the following Python packages:

     plaintext
     Copy code
     opencv-python==4.6.0.66
     Pillow==9.2.0
     face_recognition==1.3.0


## Installation
Clone the repository:

    git clone https://github.com/yourusername/advanced-face-attendance-system.git
    cd advanced-face-attendance-system


## Create a virtual environment and activate it:

    python3 -m venv venv
    source venv/bin/activate

## Install the required dependencies:

for Linux

     pip install -r requirements.txt
for windows

     pip install requirements_windows.txt

     
## Run the Application:

    python main.py


    
## Login:

Press the "Login" button on the main window.
The system first checks if the input is from a real person or a spoof attempt.
If the input passes the anti-spoofing test, the system checks for a face match in the database and logs the attendance.
If the user is not recognized or a spoof attempt is detected, the system displays an appropriate message.


## Logout:

Similar to the login process, the system verifies the user through anti-spoofing before logging the user out.


## Register a New User:

Click the "Register New User" button.
Enter the username in the prompted window and capture the image.
The system will save the facial data and associate it with the provided username.


## Project Structure
     main.py: The main application script, handling GUI, webcam feed, user login, logout, and registration, with integrated anti-spoofing.
     util.py: Contains utility functions for the application, including button creation, image processing, face recognition, and anti-spoofing integration.
     db/: Directory where user face encodings are stored.
     log.txt: Attendance log file that stores login and logout timestamps of users.

     
## How It Works
    Face Detection and Recognition: Utilizes the face_recognition library to detect and identify users.
    Anti-Spoofing: Incorporates a pre-trained model to verify if the detected face is from a real person or a spoof.
    Database: Stores user face encodings in .pickle files for fast lookup during recognition.




