# Robot Facial Expression Module
Robot Facial Expression Module

Work in Progress.

This source code have been implimented based on Ubuntu 22.04 (64bit)


Running environment is as follows:
```
CPU: Intel(R) Core(TM) i7-1165G7 @ 2.80GHz
Python: 3.9
```

## How to prepare
Create Virtual Environment.
```
conda create -n FacialExpression python=3.9
```

Download Facial Animation files and save it into './FacialExpression/animation/'
*IF THERE IS NO DIRECTORY, JUST MAKE IT'.
```
Download link: work in progress
```

## How to run
it is possible that an extra library needs to be installed to run this source code.
```
python main.py
```

## Citation

Please cite [deepface](https://ieeexplore.ieee.org/document/9259802) and [DDRL](https://ieeexplore.ieee.org/abstract/document/8451494) in your publications if it helps your research. Here is an example BibTeX entry:

```BibTeX
@inproceedings{serengil2020lightface,
  title={LightFace: A Hybrid Deep Face Recognition Framework},
  author={Serengil, Sefik Ilkin and Ozpinar, Alper},
  booktitle={2020 Innovations in Intelligent Systems and Applications Conference (ASYU)},
  pages={23-27},
  year={2020},
  doi={10.1109/ASYU50717.2020.9259802},
  organization={IEEE}
}
```

```BibTeX
@inproceedings{yu2018deep,
  title={Deep discriminative representation learning for face verification and person re-identification on unconstrained condition},
  author={Yu, Jongmin and Ko, Donghwuy and Moon, Hangyul and Jeon, Moongu},
  booktitle={2018 25th IEEE International Conference on Image Processing (ICIP)},
  pages={1658--1662},
  year={2018},
  organization={IEEE}
}
```
* FOr Facial Expression Recognition a method of the following paper is used.
Please cite [Shi et al.,](https://arxiv.org/abs/2103.10189) 
```BibTeX
@article{shi2021learning,
  title={Learning to amend facial expression representation via de-albino and affinity},
  author={Shi, Jiawei and Zhu, Songhao},
  journal={arXiv preprint arXiv:2103.10189},
  year={2021}
}
```
