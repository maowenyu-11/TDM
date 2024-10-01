# DreamMiss
## Reproduce the results
### Zhihu
```
nohup python -u DreamMiss.py --data zhihu --timesteps 1000 --lr 0.01 --beta_sche linear --w 4 --cuda 7 --eval 5 --optimizer adamw --diffuser_type mlp1 --random_seed 100 >> log/dreammiss_zhihu.log 2>&1 &
```
### YooChoose
```
nohup python -u DreamMiss.py --data yc --timesteps 2000 --lr 0.0001 --beta_sche linear --w 2 --cuda 7 --optimizer adamw --diffuser_type mlp1 --random_seed 100 >> log/dreammiss_yc.log 2>&1 &
```
### KuaiRec

```
nohup python -u DreamMiss.py --data ks --eval 5 --epoch 30 --timesteps 2000 --lr 0.00005 --beta_sche linear --w 2 --cuda 7 --optimizer adamw --diffuser_type mlp1 --random_seed 100 --linespace 100 >> log/dreammiss_ks.log 2>&1 &
 
```
