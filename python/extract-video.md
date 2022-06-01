mkdir py-yt-extract
cd py-yt-extract

python3 -m venv py-yt-extract
source py-yt-extract/bin/activate

pip3 install pytube

import cv2


import cv2
vidcap = cv2.VideoCapture('Shanti Dope - Maya (Official Music Video).mp4')
success,image = vidcap.read()
count = 0
while success:
  cv2.imwrite("frames/frame%d.jpg" % count, image)     # save frame as JPEG file      
  success,image = vidcap.read()
  print('Read a new frame: ', success)
  count += 1

print(count)