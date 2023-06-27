# ViBe-H
This repository contains the windows binary (.exe) that produces the background results of ViBe algorithm + Motion compensation via homography.

ViBe alogorithm is a background modeling method through the sample consensus, and it works well on the stationary camera.
We extend this ViBe algorithm by adopting the motion compensation from the Homography calculated by two consecutive frames.

Details are provided the following paper: <a href="">Link</a>


About the test video
--------------------------------------------------------------------------------

"woman.mp4"  is from    the    [FragTrack
Website](http://www.cs.technion.ac.il/~amita/fragtrack/fragtrack.htm).   If  you
use  it,  please   cite,  Amit  Adam,  Ehud  Rivlin,   Ilan  Shimshoni:  "Robust
Fragments-based  Tracking  using the  Integral  Histogram."   Proc.  CVPR  2006,
pp. 798-805

"continousPan.mp4"  is from    the    [Change detection dataset 2014](http://jacarini.dinf.usherbrooke.ca/dataset2014).   If  you
use  it,  please   cite,  Amit  Adam,  Ehud  Rivlin,   Ilan  Shimshoni:  "Robust
Fragments-based  Tracking  using the  Integral  Histogram."   Proc.  CVPR  2006,
pp. 798-805


}

Important notice
--------------------------------------------------------------------------------

* The code that we  ditributed earlier through e-mail had an  issue that it only
  gave good results with MS compiler. There was a bug that abs function was used
  instead of fabs (the floating point version)

* This repository is  not finalized. The current version cannot  save results as
  video,  and is  also  using  a very  old  open cv  style.   We  intend to  fix
  these. Also, there are some redundant relics from old codes.

* Again, this repository is build from a very old backup I had. You can go ahead
  an try,  as the detection  results won't change, but  bare in mind  that there
  might be compiler related issues.

How to compile and test
--------------------------------------------------------------------------------

Simply use CMake and target the output directory as "build" in the same level as
"src". In command line this would be (from the project root folder)

> project_root >> mkdir build

> project_root >> cd build

> project_root/build >> cmake ..

> project_root/build >> make

Once it is built, you can try running

> project_root/build >> ./fastMCD ../data/woman.mp4 0

When using it as a part of your program
--------------------------------------------------------------------------------










If this is helpful of your research, please cite the following paper entry (bibtex).

```BibTeX
@article{yun2013BMem,
  title={Background Memory Assisted Zero-Shot Video Object Segmentation for Unmanned Aerial and Ground Vehicles},
  author={Yun, Kimin and Hyungil, Bae, Kangmin and Moon, Jinyoung},
  journal={ETRI Journal},
  year={2023},
}

@inproceedings{yun2021unsupervised,
  title={Unsupervised moving object detection through background models for ptz camera},
  author={Yun, Kimin, Kim, Hyungil, Bae, Kangmin and Park, Jongyoul},
  booktitle={25th International Conference on Pattern Recognition (ICPR)},
  pages={3201--3208},
  year={2021},
  organization={IEEE}
}
```

