# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save and image as filename.jpg

### Step2:
Use imread(filename, flags) to read the file.

### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:
Split and merge the image using cv2.split and cv2.merge commands

### Step5:
End the program and close the output image windows.

## Program:

## Developed By : N Sandhya Charu
## Register Number : 212220230041


### i) Convert BGR and RGB to HSV and GRAY
```python3

#BGR2HSV & #RGB2HSV

hsv_image = cv2.cvtColor(house_color_image,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_image)
hsv_image1 = cv2.cvtColor(house_color_image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

#BGR2GRAY & #RGB2GRAY

gray_image = cv2.cvtColor(house_color_image,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray_image)
gray_image1 = cv2.cvtColor(house_color_image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### ii)Convert HSV to RGB and BGR
```python3

RGB_image = cv2.cvtColor(house_color_image,cv2.COLOR_HSV2RGB)
cv2.imshow('RGB2GRAY',RGB_image)
BGR_image = cv2.cvtColor(house_color_image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR',BGR_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

### iii)Convert RGB and BGR to YCrCb
```python3

YCrCb_image = cv2.cvtColor(house_color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### iv)Split and Merge RGB Image
```python3

Blue = RGB_image[:,:,0]
Green = RGB_image[:,:,1]
Red = RGB_image[:,:,2]
cv2.merge((Red,Blue,Green))
cv2.merge((Blue,Green,Red))
cv2.imshow("RED",Red)
cv2.imshow("BLUE",Blue)
cv2.imshow("GREEN",Green)
Merged = cv2.merge([Red,Blue,Green])
cv2.imshow('Rgb',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

### v) Split and merge HSV Image
```python3

h, s, v = cv2.split(hsv_image)
cv2.merge((h,s,v))
cv2.imshow("h plane",h)
cv2.imshow("s plane",s)
cv2.imshow("v plane",v)
merged = cv2.merge([h,s,v])
cv2.imshow('hsv_merge',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### i) BGR and RGB to HSV and GRAY

![Screenshot (1)](https://user-images.githubusercontent.com/75235167/162724334-745ec24e-7ab8-40a2-8756-e61b1d235402.png)

![Screenshot (1)](https://user-images.githubusercontent.com/75235167/162724728-d7874fa2-6160-4f5d-aaaf-1736b9a2e702.png)

### ii) HSV to RGB and BGR

![Screenshot (1)](https://user-images.githubusercontent.com/75235167/162724908-58840217-b548-452e-aa92-3ae2ce7e3289.png)

### iii) RGB and BGR to YCrCb

![Screenshot (1)](https://user-images.githubusercontent.com/75235167/162725074-01014b34-bb1f-40d9-a4e0-8f3fdebca609.png)

### iv) Split and merge RGB Image

![Screenshot (1)](https://user-images.githubusercontent.com/75235167/162726060-28c180f5-05c5-4117-84b5-e82a0309ed29.png)

![Screenshot (1)](https://user-images.githubusercontent.com/75235167/162726211-b73398ce-bd13-4a89-b242-317c45d962d4.png)


### v) Split and merge HSV Image

![Screenshot (1)](https://user-images.githubusercontent.com/75235167/162725492-c38d29a8-b1c7-4a04-9c1e-e38a74a231a4.png)

![Screenshot (1)](https://user-images.githubusercontent.com/75235167/162725692-1eee0ae6-5cc1-45a1-88e2-846e4fce6110.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
