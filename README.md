## 📌 Overview

This project performs **real-time instance segmentation** — detecting objects, classifying them, and generating a pixel-level mask for each individual instance — directly from a live webcam stream.

It uses a **Mask R-CNN** model with a ResNet-101 + FPN backbone, trained on the **MS COCO** dataset (80 common object classes) using pre-trained weights. Unlike bounding-box detectors, Mask R-CNN outlines the exact shape of every object, making it useful for scene understanding, autonomous-driving perception, and video analytics.

---

## 🎬 Demo

| Demo | Link |
| --- | --- |
| Instance segmentation from webcam | [▶ Watch on YouTube](https://youtu.be/2YfW8VDSvZo) |
| Tested on busy Indian roads | [▶ Watch on YouTube](https://www.youtube.com/watch?v=o6XQ79yozO8) |

### Sample results

![Road vehicles](https://user-images.githubusercontent.com/19996897/38748412-a02387ac-3f6b-11e8-8c67-371fdf0d0a1f.png)
![Road scene](https://user-images.githubusercontent.com/19996897/38748414-a1fd2b78-3f6b-11e8-92aa-806038e37c2d.png)
![Vehicles on road](https://user-images.githubusercontent.com/19996897/38748425-a7088004-3f6b-11e8-93c0-7e020aa7c0f9.png)
![Indian roads](https://user-images.githubusercontent.com/19996897/38748438-b3b56614-3f6b-11e8-9e8f-eacca943e460.png)
![Indian road detail](https://user-images.githubusercontent.com/19996897/38748442-b716ca46-3f6b-11e8-8f19-a09786e36ffa.png)

---

## ✨ Features

- **Real-time inference** on a live webcam feed via OpenCV
- **Instance-level segmentation** — separate mask, class label, and confidence score per object
- **80 object classes** out of the box (MS COCO: people, vehicles, animals, everyday objects)
- Uses **pre-trained COCO weights** — no training required to get started
- Easily extensible to custom datasets and additional classes

---

## 🛠️ Requirements

```text
Python >= 3.4
numpy
scipy
Pillow
cython
matplotlib
scikit-image
tensorflow >= 1.3.0
keras >= 2.0.8
opencv-python
h5py
imgaug
IPython[all]
pycocotools
```

Install everything with:

```bash
pip install -r requirements.txt
```

---

## 🚀 Getting Started

**1. Clone the repository**

```bash
git clone https://github.com/SrikanthVelpuri/Mask_RCNN.git
cd Mask_RCNN
```

**2. Install dependencies**

```bash
pip install -r requirements.txt
```

**3. Download the pre-trained COCO weights**

Download `mask_rcnn_coco.h5` from the [releases page](https://github.com/matterport/Mask_RCNN/releases) and place it in the project root.

**4. Run real-time segmentation from your webcam**

```bash
python webcam.py
```

Press **`q`** to quit the live window.

---

## 🧠 How It Works

Mask R-CNN extends Faster R-CNN with a parallel branch that predicts a segmentation mask for each detected object:

1. A **backbone** (ResNet-101 + FPN) extracts feature maps from the input frame.
2. A **Region Proposal Network (RPN)** proposes candidate object regions.
3. **RoIAlign** precisely pools features for each region.
4. Three parallel heads output the **class**, **bounding box**, and **binary mask** per instance.

---

## 📈 Performance & Possible Improvements

This model was tested on an **NVIDIA 840M (4 GB)**, which limits the frame rate. Recommended upgrades:

- **Faster hardware** — an NVIDIA Titan X / 1080 Ti (or a modern RTX GPU) can roughly double the frame rate.
- **More classes** — the current model detects the 80 COCO classes; training on additional datasets expands the range of recognizable objects.
- **Lighter backbones** — swapping to ResNet-50 or a mobile backbone trades some accuracy for higher FPS.

---

## 🙏 Acknowledgements

This implementation is built on the excellent [**Matterport Mask R-CNN**](https://github.com/matterport/Mask_RCNN) and the original paper:

> **Mask R-CNN** — Kaiming He, Georgia Gkioxari, Piotr Dollár, Ross Girshick (2017). [arXiv:1703.06870](https://arxiv.org/abs/1703.06870)

Trained and evaluated on the [MS COCO](https://cocodataset.org/) dataset.

---

## 📄 License

Released under the **MIT License**. See the `LICENSE` file for details.

---

<p align="center">
  Built by <a href="https://github.com/SrikanthVelpuri">Srikanth Velpuri</a> · ⭐ Star the repo if you find it useful!
</p> 
        
