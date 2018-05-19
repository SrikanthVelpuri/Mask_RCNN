# Mask_RCNN  using Webcam

#### Requirements

    Python>=3.4
    numpy
    scipy
    Pillow
    cython
    matplotlib
    scikit-image
    tensorflow>=1.3.0
    keras>=2.0.8
    opencv-python
    h5py
    imgaug
    IPython[all]
    pycocotools

### Model is trained MS COCO dataset and pre-trained weights are used for instance segmentation of the objects using Webcam 

Here is the sample video of instance segmentation of objects using Mask-RCNN
https://youtu.be/2YfW8VDSvZo

Sample video of this model tested on Busy Indian Roads : https://www.youtube.com/watch?v=o6XQ79yozO8

### Sample Images tested using Mask-RCNN

![roadvehicles](https://user-images.githubusercontent.com/19996897/38748412-a02387ac-3f6b-11e8-8c67-371fdf0d0a1f.png)
![road](https://user-images.githubusercontent.com/19996897/38748414-a1fd2b78-3f6b-11e8-92aa-806038e37c2d.png)
![vehiclesonroad](https://user-images.githubusercontent.com/19996897/38748425-a7088004-3f6b-11e8-93c0-7e020aa7c0f9.png)
![indianroads](https://user-images.githubusercontent.com/19996897/38748438-b3b56614-3f6b-11e8-9e8f-eacca943e460.png)
![indianroad1](https://user-images.githubusercontent.com/19996897/38748442-b716ca46-3f6b-11e8-8f19-a09786e36ffa.png)

# Possible Improvements
 This model is implemented using Nvidia 840M with 4GB memory, so the frame rate is very less.For getting better frame rates we can use Nvidia Titan X or Nvidia 1080Ti.By using these graphic cards we can double the frame rate of the present Scenario.
 Right Now only 80 common objects can be detected, but if we train this on multiple datasets then we can increase the types of objects detetected.    
        
