# Welcome to TDM!
This is an official implementation of ***Addressing Missing Data Issue for Diffusion-based Recommendation***, which is accepted by SIGIR'2025.

## Algorithms 
The training and generating phases of TDM are as follows.

<img src="https://github.com/maowenyu-11/TDM/blob/main/algorithm.png" 
     width="50%" 
     style="max-width: 500px;">


## Reproduce the results

Our experiment settings are specified in the `TDM.yml` file. To create the environment, you can use the following command:

```
conda env create -f TDM.yml

```

### Zhihu
```
nohup python -u TDM.py --data zhihu --timesteps 1000 --lr 0.01 --beta_sche linear --w 6 --cuda 6 --eval 5 --optimizer adamw --diffuser_type mlp1 --random_seed 100 >> log/TDM_zhihu.log 2>&1 &

```
### YooChoose
```
nohup python -u TDM.py --data yc --timesteps 2000 --lr 0.0001 --beta_sche linear --w 0 --cuda 7 --optimizer adamw --diffuser_type mlp1 --random_seed 100 >> log/TDM_yc.log 2>&1 &

```
### KuaiRec

```
nohup python -u TDM.py --data ks --eval 5 --epoch 30 --timesteps 2000 --lr 0.00005 --beta_sche linear --w 2 --cuda 4 --optimizer adamw --diffuser_type mlp1 --random_seed 100 --linespace 100 >> log/TDM_ks.log 2>&1 &

```

## Citation

❤ If you find our repository useful in your research, please star us ⭐ and consider citing:

```
@inproceedings{mao2025TDM,
  title={Addressing Missing Data Issue for Diffusion-based Recommendation},
  author={Wenyu Mao, Zhengyi Yang, Jiancan Wu, Haozhe Liu, Yancheng Yuan, Xiang Wang, Xiangnan He},
  booktitle={Proceedings of the 48th International ACM SIGIR Conference on Research and Development in Information Retrieval. 2025},
  year={2024}
}
```
