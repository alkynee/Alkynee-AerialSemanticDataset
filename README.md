
<p align="center">
 <img src="https://github.com/alkynee/Alkynee-AerialSemanticDataset/blob/main/readme_images/frame271-ok.jpg" width=150 height=150 alt="centered logo" />
 </p>
<h1 align="center">Alkynee Aerial Semantic Dataset</h1>

This is an aerial image dataset for semantic scene understanding under active development.

## LOG
|Date   | Log  |
|---|---|
| 2019.09.01  | Initialization  |
| 2021.09.23  |  Alkynee Aerial Semantic Dataset released |


## Dataset Overview:
- Alkynee Aerial Semantic Dataset
| class  | GT  | (R, G, B)  |
|---|---|---|
| _background_ | 0   | (0, 0, 0)  |
| _road_ |  1 |  (128, 0, 0) |
| _occluded_road_ |  2 | (0, 128, 0)  |
| _vegetation_ |  3 | (128, 128, 0)  |

## Directory Structure:
```
Alkynee Aerial Semantic Dataset
│
└─── readme_images
|
└─────────data
│          |
│          └─── train
|          |       └───| images 
|          |       └───| gray_masks
|          |       └───| rgb_masks
|          └───   val
|          |       └───| images 
|          |       └───| gray_masks
|          |       └───| rgb_masks
|          |        
|          |    .gitignore
|          ...
└───utils
│   │  label_generator.py
│   │  labels.txt 
│   │  requirements.txt
│   ...
│   
|   .gitignore
|    CITATION.cff
|    LICENSE
|    README.md
|   ...
```

DESCRIPTION:<br />
|Folder Name| Description |
|---|---|
| train| contains three folders as images, rgb_masks, gray_masks|
| val| contains three folders as images, rgb_masks, gray_masks|
| images  | Aerial images captured by DJI Phantom 4 drone  |
| rgb_masks | RGB masks of the corresponding images generated after annotations  |
|  gray_masks    | Gray scale masks of the corresponding images     |
| utils  | Important files related to dataset preparation  |


## Benchmark
The benchmark is available to seek improved solutions for the proposed dataset. The metrics used are OA (Overall Accuracy/pixelwise accuracy), mIoU (mean Intersection over Union). Researchers are encouraged to contribute!


-Obtained Results
| Models  | #Parameters  | OA | mIoU |
|---------|--------------|----|------|
|FCN-8s   |   136*M*           |  0.72  |  0.16     |
|FCN-16s   |  134*M*            | 0.83   | 0.68     |
|FCN-32s   |  134*M*            | 0.86   | 0.63     |
|FC_Densenet_103   |  9.42*M* | 0.91   | 0.62     |
|E-Net   |     350.65*K*         | 0.89   | 0.65    |
|LinkNet   |   1.15*M*           | 0.93  |  0.46    |


## Sample Images
<table>
     
  <tr>
    <td>image</td>
     <td>mask</td>
  </tr>
  <tr>
    <td><img src="https://github.com/alkynee/Alkynee-AerialSemanticDataset/blob/main/readme_images/imgs/NITR_AC_JAN26_30.jpg" width=480 height=270></td>
    <td><img src="https://github.com/alkynee/Alkynee-AerialSemanticDataset/blob/main/readme_images/seg_class/NITR_AC_JAN26_30.png" width=480 height=270></td>
  </tr>
  <tr>
    <td><img src="https://github.com/alkynee/Alkynee-AerialSemanticDataset/blob/main/readme_images/imgs/NITR_FR_1.jpg" width=480 height=270></td>
    <td><img src="https://github.com/alkynee/Alkynee-AerialSemanticDataset/blob/main/readme_images/seg_class/NITR_FR_1.png" width=480 height=270></td>
  </tr>
  <tr>
    <td><img src="https://github.com/alkynee/Alkynee-AerialSemanticDataset/blob/main/readme_images/imgs/NITR_FR_6.jpg" width=480 height=270></td>
    <td><img src="https://github.com/alkynee/Alkynee-AerialSemanticDataset/blob/main/readme_images/seg_class/NITR_FR_6.png" width=480 height=270></td>
  </tr>
 </table>

## Download Link:
- Alkynee Aerial Semantic Dataset: (train+val) <br />
[GDrive](https://drive.google.com/drive/folders/1IQUadXFpEFEsB_9I5JVUuGJBjqIL5MFG?usp=sharing)


## LICENSE:

This dataset is licensed to Visual Surveillance Laboratory, Department of Computer Science and Engineering, National Institute of Technology, Rourkela, India. 

## Citation & Acknowledgements

This dataset is publicly available for non-commercial use only. If you use this dataset in your research or wish to refer to the baseline results, please cite the work with the following annotation:

    @article{AlkyneeAerialSemanticDataset2021,
        title={The Alkynee Aerial Semantic Dataset: Addressing Challenges in Road Extraction from Aerial Images},
        author={Behera, Tanmay Kumar and Bakshi, Sambit and Sa, Pankaj Kumar and Nappi, Michael and Castiglione, Aniello and Vijayakumar, Pandi   and Gupta, Brij},        
        journal = {Journal of Signal Processing Systems},
        publisher={Springer},
        year={2021}, 
        note = "doi:10.1007/s11265-022-01777-0"
     }
   