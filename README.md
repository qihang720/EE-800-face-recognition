# EE-800-face-recognition
There are 4 files.

Gather_example.py is used to cut videos to images, which can used in dataset. 
Command: 1. python gather_example.py --input videos/qihangreal.mov --output dataset/real/qihangreal --detector face detector --skip 1
2. python gather_example.py --input videos/fake1.mov --output dataset/real/fake1 --detector face detector --skip 1
Skip can control cut frequence. 

Livenessnet.py is the vgg network file. It will used in train.py.

Train.py load input dataset, including fake and real, to build a vgg network.
Command: python train.py --dataset --model liveness.model --le le.pickle --plot 1.png

Liveness_demo.py can detect face in front of camera. It will apply liveness.model and le.pikle. 
Command: python liveness_demo.py  --model liveness.model --le le.pickle  --detector face_detector
