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