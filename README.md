## Image_Acqusition-_using_Web_Camera
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
<br>
Import OpenCV Package.

### Step 2:
<br>
Capture Video from Webcam. Use VideoCapture(0) to access the webcam and start capturing video.

### Step 3:
<br>
Read Video or Image. Utilize 'imread' to read a video frame or image from the webcam.

### Step 4:
<br>
Save Image to File. Employ 'imwrite' to save the captured image to a file.

### Step 5:
<br>
Display Video or Image. Use 'imshow' to display the captured video frame or image.

### Step 6:
<br>
End Program with 'q'. Allow the program to be terminated by pressing the 'q' key.

## Program:
### Developed By: JANANI S
### Register No: 212223230086
``` Python

## i) Write the frame as JPG file

import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()
captured_image = cv2.imread('captured_frame.jpg')
plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()


## ii) Display the video

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()

## iii) Display the video by resizing the window


cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
  
## iv) Rotate and display the video

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release() 

```
## Output

### i) Write the frame as JPG image
</br>
<img width="707" height="517" alt="image" src="https://github.com/user-attachments/assets/88d24644-1257-4a10-82c9-3c1c7a536c12" />

</br>


### ii) Display the video
</br>
<img width="682" height="491" alt="image" src="https://github.com/user-attachments/assets/a045268b-601d-4cd4-9489-88f164d5672f" />

</br>


### iii) Display the video by resizing the window
</br>
<img width="378" height="488" alt="image" src="https://github.com/user-attachments/assets/d783d7fa-679f-4d20-897c-047d58264cc4" />

</br>



### iv) Rotate and display the video
</br>
<img width="406" height="498" alt="image" src="https://github.com/user-attachments/assets/7def23bd-4bb1-4cd2-9965-7ac8781b33de" />

</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
