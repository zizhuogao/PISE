# PISE

The code for our CVPR paper [PISE: Person Image Synthesis and Editing with Decoupled GAN](https://arxiv.org/abs/2103.04023)

# Requirement

```
conda create -n pise python=3.6
conda install pytorch=1.2 cudatoolkit=10.0 torchvision
pip install scikit-image pillow pandas tqdm dominate natsort 
```

# Data

Data preparation for images and keypoints can follow [Pose Transfer](https://github.com/tengteng95/Pose-Transfer)


Parsing data can be found from [baidu](https://pan.baidu.com/s/19boQPJnrq2wASSMqzl27NQ) (fectch code: abcd) or [Google drive](https://drive.google.com/file/d/1AcK4fuYOZw0i2Gi_X7kGdO3ffosIIUnj/view?usp=sharing).



# Train

```
python train.py --name=fashion --model=painet --gpu_ids=0
```
**Note that if you want to train a pose transfer model as well as texture transfer and region editing, just comments the line 177 and 178, and uncomments line 162-176.**


# Test

You can directly download our test results from [baidu](https://pan.baidu.com/s/16HiFP6hExXVSzbs9A_Bhbw) (fetch code: abcd) or [Google drive](https://drive.google.com/file/d/1u62gyQ46_qZGB6BlESpk0WLjcZ-NH8-F/view?usp=sharing). <br>
Pre-trained checkpoint of human pose transfer reported in our paper can be found from [baidu](https://pan.baidu.com/s/14v3LaCCGCHJUoqQ_wlyNpA) (fetch code: abcd) or [Google drive](https://drive.google.com/file/d/1gcdzahJ-pE-bSQfcnrW__iXIViH_y-FB/view?usp=sharing) and put it in the folder (-->results-->fashion). 

Pre-Trained checkpoint of texture transfe, region editing, style interpolation used in our paper can be found from [baidu](https://pan.baidu.com/s/1E025k57INvL0O8cdLi87og)(fetch code: abcd) or [Google drive](https://drive.google.com/file/d/1fMFBIkU1AEQaa3vbhba3oV0rU5YSr7GR/view?usp=sharing). Note that the model need to be changed.

**Test by yourself** <br>


```
python test.py --name=fashion --model=painet --gpu_ids=0 
```


# Citation

If you use this code, please cite our paper.

```
@inproceedings{PISE,
  title={{PISE}: Person Image Synthesis and Editing with Decoupled GAN},
  author={Jinsong, Zhang and Kun, Li and Yu-Kun, Lai and Jingyu, Yang},
  booktitle={Computer Vision and Pattern Recognition (CVPR)},
  year={2021}
}
```

# Acknowledgments

Our code is based on [GFLA](https://github.com/RenYurui/Global-Flow-Local-Attention).









