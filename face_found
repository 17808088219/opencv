import cv2

frontalface = cv2.CascadeClassifier("D:\Python_WorkPlace\cascade_lib/haarcascade_frontalface_default.xml")          # 训练库地址信息

capture = cv2.VideoCapture(0)          #打开摄像头
while True:
    ret, frame = capture.read()        #读取摄像头
    frame = cv2.flip(frame,1)           #镜像操作
    gray_photo = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)        #灰度化

    face=frontalface.detectMultiScale(gray_photo,1.3,5)             #找到人脸
    for(x,y,w,h) in face:                                            #画人脸
        img = cv2.rectangle(frame,(x,y),(x+w,y+h),(255,0,0),2)

    cv2.imshow("video", frame)
    if cv2.waitKey(50)&0xff == ord("q"):
        break

cv2.destroyAllWindows()
