[![GitHub issues](https://img.shields.io/github/issues/amine0110/preporcess-volume-medical-imaging)](https://github.com/amine0110/preporcess-volume-medical-imaging/issues) [![GitHub stars](https://img.shields.io/github/stars/amine0110/preporcess-volume-medical-imaging)](https://github.com/amine0110/preporcess-volume-medical-imaging/stargazers) [![GitHub license](https://img.shields.io/github/license/amine0110/preporcess-volume-medical-imaging)](https://github.com/amine0110/preporcess-volume-medical-imaging) ![PyPI - Python Version](https://img.shields.io/pypi/pyversions/torch) [![YouTube Video Views](https://img.shields.io/youtube/views/83FLt4fPNGs?style=social)](https://www.youtube.com/watch?v=83FLt4fPNGs&t=2s) ![GitHub watchers](https://img.shields.io/github/watchers/amine0110/preporcess-volume-medical-imaging?style=social)
# Preprocessing 3D Volumes for Tumor Segmentation using PyTorch and Monai

## Introduction 
Regarding the difficulties that we can encounter when using traditional image processing tools, deep learning has emerged as the primary solution in the healthcare field.

Because medical images are more difficult to process than standard images (dense contrast, a wide range of variations in the human body…) Deep learning is used for classification, object detection, and especially segmentation tasks.

When it comes to segmentation, deep learning is used to segment human organs such as the liver, lung, and… or to segment tumors from different parts of the body.

## Tools we will use
To complete this task, we will use an open source framework called `monai`, which is based on `PyTorch`, which I used during my internship and found to be very useful.

## Little explanation
When using `monai`, you don't need to create any 2D images because it uses directly the 3D volumes. Here is the example of opening a 3D volume then convert it into a torch tensor:

```Python
orig_transforms = Compose(

    [
        LoadImaged(keys=['image', 'label']),
        AddChanneld(keys=['image', 'label']),
        
        ToTensord(keys=['image', 'label'])
    ]
)
```

-----------------------------------------------------------

For more information, you can read my [blog post](https://pycad.co/preprocessing-3d-volumes-for-tumor-segmentation-using-monai-and-pytorch/) about this repo or you can watch my [YouTube video](https://youtu.be/83FLt4fPNGs).

## 📩 Newsletter
Stay up-to-date on the latest in computer vision and medical imaging! Subscribe to my newsletter now for insights and analysis on the cutting-edge developments in this exciting field.

https://pycad.co/join-us/

## 🆕 NEW 

Learn how to effectively manage and process DICOM files in Python with our comprehensive course, designed to equip you with the skills and knowledge you need to succeed.

https://www.learn.pycad.co/course/dicom-simplified


