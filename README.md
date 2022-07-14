
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
