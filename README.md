import cv2
import matplotlib as plt
import easyocr

image_path ='photos/asd.jpg'
img = cv2.imread(image_path)

reader = easyocr.Reader(['en'] , gpu = False)
text_ = reader.readtext(img)
for t in text_:
    print (t)
    bbox , text,  score =t


   # cv2.rectangle(img,bbox[0], (0, 255, 0), 5)



#plt.imshow(img, cv2.COLOR_BGR2RGB)
#plt.show()


