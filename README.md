# ViBe-H
This repository houses the Windows executable (.exe) that implements the ViBe algorithm with additional motion compensation via homography, the foundation of our background results. 
The ViBe algorithm is a robust background modeling method that operates based on sample consensus, performing optimally with stationary cameras. Our extension to this algorithm involves the integration of motion compensation derived from homography, calculated from two successive frames.

Further details regarding this implementation are described in our research paper, available here: <a href="">Link</a>




Usage
--------------------------------------------------------------------------------
First, open your Windows terminal, navigate to the location where the .exe file is located, and execute the following command:

vibeH.exe <video_path> <option>

<option>
0: Displays the original frame and background image. 
  
1: A "result" directory is created, and several result files (jpeg images) are saved. Display off.

Example:

```bash
vibeH.exe "woman.mp4" 0
```

```bash
vibeH.exe "continuousPan.mp4" 1
```

Environment
--------------------------------------------------------------------------------
Windows OS, OpenCV 3.4.2


Related Projects 
--------------------------------------------------------------------------------

* https://github.com/vcg-uvic/fastMCD
  - This is the base paper for our research, and the source code is publicly available (C++, Python).

* https://github.com/CansenJIANG/SCBU
  - This is the executable file for the results of a paper published in Pattern Recognition Letters in 2017, which supports the feature of foreground saving.


About the Test Videos
--------------------------------------------------------------------------------

The "woman.mp4" video was sourced from the [FragTrack Website](http://www.cs.technion.ac.il/~amita/fragtrack/fragtrack.htm). If you use this video, please cite the following paper: Amit Adam, Ehud Rivlin, Ilan Shimshoni. "Robust Fragments-based Tracking using the Integral Histogram." Proc. CVPR 2006, pp. 798-805.

The "continuousPan.mp4" video is part of the PTZ series from the [ChangeDetection2014 dataset](http://jacarini.dinf.usherbrooke.ca/dataset2014). If you utilize this video, please cite the following paper: Y. Wang, P.-M. Jodoin, F. Porikli, J. Konrad, Y. Benezeth, and P. Ishwar. "CDnet 2014: An Expanded Change Detection Benchmark Dataset." Proc. IEEE Workshop on Change Detection (CDW-2014) at CVPR-2014, pp. 387-394, 2014.



License and Citation
--------------------------------------------------------------------------------

Copyright (c) 2023 Kimin Yun.
All rights reserved.

This software is strictly for non-commercial use only due to institutional policies limiting the public disclosure of the source code. For commercial use or to acquire the source code or its usage rights, companies located in South Korea can process the technology transfer through the associated fees according to our institution policy. For more information about this process, please contact me at kimin.yun (at) gmail.com or kimin.yun (at) etri.re.kr.

Additionally, if this work contributes to your research and is used for academic purposes, please cite our paper as follows:


```BibTeX
@article{yun2023BMem,
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

