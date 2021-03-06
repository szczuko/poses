Detailed documentation of this dataset can be found in:

P. Szczuko. ANN for human pose estimation in low resolution depth images. IEEE Conf Signal Processing: Algorithms, Architectures, Arrangements, and Applications (SPA), pp. 354-359, 2017, https://doi.org/10.23919/SPA.2017.8166892 (requires login to IEEE)

P. Szczuko. CNN Architectures for Human Pose Estimation from a Very Low Resolution Depth Image, 11th Conf. HSI Human System Interaction 2018, pp. 118-124, https://doi.org/10.1109/HSI.2018.8431338  (requires login to IEEE)

and comparison of models (my DNNN33 plus "transfer-learned" models of **SqueezeNet, MobileNet SSD, ResNet, VGG**) **performance** on this dataset is published in:

P. Szczuko. Deep Neural Networks for Human Pose Estimation from a Low Resolution Depth Image, Multimedia Tools and Applications Journal 2019, https://doi.org/10.1007/s11042-019-7433-7 (open access from Springer, without login)

The file is currently avaiable at dropbox:
https://goo.gl/XWrgN5

This is 317MB 7z archive containing csv file, 3.6GB large.

Columns are as follows:

- scale (fixed, not used)
- camX,camY,camZ (camera localization, can be used for calculating relative distances or coordinates)
- IKRx,IKRy,IKRz (Inverse kinematics of forearm-arm-hand were used to position the model, those are coordinates of the target for **right wrist**)
- IKTRx,IKTRy,IKTRz  (In the Inverse kinematics the **right elbow** was pointing to those coordinates)
- IKLx,IKLy,IKLz  (the same as above but for **left wrist**)
- IKTLx,IKTLy,IKTLz (the same as above but for **left elbow**)
Positions of each key joints
- RightArmX,RightArmY,RightArmZ - absolute coordinates in the **3D space**
- RightArmIX,RightArmIY - coordinates on the **image plane** (number of pixel row and column)
- the same format for all other joints: RightForeArmX,RightForeArmY,RightForeArmZ, RightForeArmIX,RightForeArmIY, RightHandX,RightHandY,RightHandZ, RightHandIX,RightHandIY, LeftArmX,LeftArmY,LeftArmZ, LeftArmIX,LeftArmIY, LeftForeArmX,LeftForeArmY,LeftForeArmZ, LeftForeArmIX,LeftForeArmIY, LeftHandX,LeftHandY,LeftHandZ, LeftHandIX,LeftHandIY, HeadX,HeadY,HeadZ, HeadIX,HeadIY, NeckX,NeckY,NeckZ, NeckIX,NeckIY, Spine1X,Spine1Y,Spine1Z, Spine1IX,Spine1IY, HipsX,HipsY,HipsZ, HipsIX,HipsIY, RightLegX,RightLegY,RightLegZ, RightLegIX,RightLegIY, LeftLegX,LeftLegY,LeftLegZ, LeftLegIX,LeftLegIY
- px1 ...up to px3050 (depth image pixels, can be interpreted as a grayscale, range 0.0 to 1.0)
