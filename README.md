# Image_Acqusition-_using_Web_Camera
## Aim
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera
<br>

### Step 2:
Use cv2.imread to read the video or image
<br>

### Step 3:
Use cv2.imwrite to save the image
<br>

### Step 4:
Use cv2.imshow to show the video
<br>

### Step 5:
End the program and close the output video window by pressing 'q'.
<br>

## Program:
``` Python
Developed By:naveen s
Register No: 212222240070
```

## i) Write the frame as JPG file
```Python
import cv2
cap = cv2.VideoCapture (0)
frame_number = 0
while frame_number < 5:
    ret, frame = cap.read()
    cv2.imshow('frame', frame)
    cv2.imwrite(f"frame_{frame_number}.jpg", frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## ii) Display the video
```Python
import cv2
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read()
    cv2.imshow('Video', frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iii) Display the video by resizing the window
```Python
import cv2
cap = cv2.VideoCapture (0) 
cv2.namedWindow('Video', cv2.WINDOW_NORMAL)
while True:
    ret, frame = cap.read()
    cv2.imshow('Video', frame)
    cv2.resizeWindow('Video', 100, 200)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iv) Rotate and display the video
```Python
import cv2
cap = cv2.VideoCapture (0)
while True:
    ret, frame = cap.read()
    rotated_frame=cv2.rotate(frame,cv2.ROTATE_90_CLOCKWISE)
    cv2.imshow('Rotated Video', rotated_frame)
    cv2.imwrite(f"frame_{frame_number}.jpg", frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output
### i) Write the frame as JPG image
![WhatsApp Image 2024-09-25 at 4 04 32 PM](https://github.com/user-attachments/assets/e1e65181-8688-4fa4-bada-d78e6dcfcd02)


</br>
</br>

### ii) Display the video
![WhatsApp Image 2024-09-25 at 4 04 34 PM](https://github.com/user-attachments/assets/0ac2fd21-695b-485c-8bcb-06f4658d1cb6)



</br>
</br>

### iii) Display the video by resizing the window
![WhatsApp Image 2024-09-25 at 4 05 50 PM](https://github.com/user-attachments/assets/bb080fd5-9389-44fd-b639-41e26b1a2708)


</br>
</br>

### iv) Rotate and display the video
![WhatsApp Image 2024-09-25 at 4 06 37 PM](https://github.com/user-attachments/assets/4c51a303-3dd4-4efc-b9ca-cc8d691fa58a)


</br>
</br>

## Result:
Thus the image is accessed from webcamera and displayed using openCV.
