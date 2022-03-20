create a black image in python
``` python
import cv2
import numpy as np

img = np.zeros((512,512,3), np.uint8)
cv2.imshow('image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

draw a circle point in python
``` python
import cv2
import numpy as np

img = np.zeros((512,512,3), np.uint8)

# cv2 use BGR color not RGB
cv2.circle(img, (447,63), 63, (0,0,255), -1)
cv2.imshow('image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

draw a line in python
``` python
import cv2
import numpy as np

img = np.zeros((512,512,3), np.uint8)
cv2.line(img, (0,0), (511,511), (255,0,0), 5)
cv2.imshow('image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

get key input in python
``` python
import cv2
import numpy as np

```

capture video from webcam in python
``` python
import cv2

cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read()
    cv2.imshow('frame', frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```

find face in image in python
``` python
import cv2
import numpy as np

def findFace(img):
    gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
    face_cascade = cv2.CascadeClassifier('haarcascade_frontalface_default.xml')
    faces = face_cascade.detectMultiScale(gray, 1.3, 5)
    for (x,y,w,h) in faces:
        cv2.rectangle(img, (x,y), (x+w, y+h), (255,0,0), 2)

    return img

cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read()
    frame = findFace(frame)
    cv2.imshow('frame', frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
```

find pallet in image in python
``` python
import cv2
import numpy as np

def findPallet(img):
    gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
    pallet_cascade = cv2.CascadeClassifier('pallet.xml')
    pallets = pallet_cascade.detectMultiScale(gray, 1.3, 5)
    for (x,y,w,h) in pallets:
        cv2.rectangle(img, (x,y), (x+w, y+h), (255,0,0), 2)

cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read()
    frame = findPallet(frame)
    cv2.imshow('frame', frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
```

### path follow in python

- when to move forward
    - [0,1,0]
- when to move backward

- when to turn left
    - [1,0,0]
- when to turn right
    - [0,0,1]
- when to stop
    - [0,0,0]
    - [1,1,1]
    - [1,0,1]
- when to slide left
    - [1,1,0]
- when to slide right
    - [0,1,1]

how to draw a path?
how to know drone's position?
how to know drone's in the path?

