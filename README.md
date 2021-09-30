# PointWOLF: Point Cloud Augmentation with Weighted Local Transformations

This repository is the implementation of PointWOLF\(To appear\).

> Sihyeon Kim<sup>1*</sup>, Sanghyeok Lee<sup>1*</sup>, Dasol Hwang<sup>1</sup>, Jaewon Lee<sup>1</sup>, Seong Jae Hwang<sup>2</sup>, Hyunwoo J. Kim<sup>1†</sup>, Point Cloud Augmentation with Weighted Local Transformations (ICCV 2021).

![PointWOLF_main](assets/PointWOLF_main.png)

# Installation
## Dependencies
- CUDA 10.2
- Python==3.7.1
- torch==1.7.0
- packages : sklearn, numpy, h5py, glob

## Download
**Clone repository**  

```
$ git clone ???
```

**Download ModelNet40**  

**Notes** : When you run the `main.py`, ModelNet40 is automatically downloaded at `.../PointWOLF/data/`.  
If you want to download dataset on `${path}`, see below.

```
$ cd ${path}
$ wget https://shapenet.cs.stanford.edu/media/modelnet40_ply_hdf5_2048.zip --no-check-certificate
$ unzip modelnet40_ply_hdf5_2048.zip
$ rm modelnet40_ply_hdf5_2048.zip
```

# Runnig the code

**train**

- Run the training without PointWOLF & AugTune:  
```
$ python main.py --exp_name=origin --model=dgcnn --num_points=1024 --k=20 --use_sgd=True
```

- Run the training with **PointWOLF**:  
```
$ python main.py --exp_name=PointWOLF --model=dgcnn --num_points=1024 --k=20 --use_sgd=True --PointWOLF
```

- Run the training with **PointWOLF** & **AugTune**:  
```
$ python main.py --exp_name=PointWOLF_AugTune --model=dgcnn --num_points=1024 --k=20 --use_sgd=True --PointWOLF --AugTune
```


**eval**

- Run the evaluation with trained model located at `${PATH}`:  
```
$ python main.py --exp_name=eval --model=dgcnn --num_points=1024 --k=20 --use_sgd=True --eval=True --model_path=${PATH}
```

# Citation


# License
MIT License

# Acknowledgement
The structure of this codebase is borrowed from [DGCNN](https://github.com/WangYueFt/dgcnn).
