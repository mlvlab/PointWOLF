# PointWOLF: Point Cloud Augmentation with Weighted Local Transformations

This repository is the implementation of [PointWOLF]().

> Sihyeon Kim<sup>1*</sup>, Sanghyeok Lee<sup>1*</sup>, Dasol Hwang<sup>1</sup>, Jaewon Lee<sup>1</sup>, Seong Jae Hwang<sup>2</sup>, Hyunwoo J. Kim<sup>1†</sup>, Point Cloud Augmentation with Weighted Local Transformations (ICCV 2021).

![PointWOLF_main](https://user-images.githubusercontent.com/49049753/129553285-d7ea163b-c5a1-4b6c-ba98-077616d2b953.png)

# Runnig the code
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

- Run the evaluation with trained model located at `${PATH}`:  
```
$ python main.py --exp_name=eval --model=dgcnn --num_points=1024 --k=20 --use_sgd=True --eval=True --model_path=${PATH}
```


# Acknowledgement
The structure of this codebase is borrowed from [Dynamic Graph CNN for Learning on Point Clouds](https://github.com/WangYueFt/dgcnn).
