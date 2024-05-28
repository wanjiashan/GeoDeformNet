 ## GeoDeformNet: Robust 3D Point Cloud Registration with Geometric Deformation Network

---



## Method overview

<img src="assets/Network Architecture Diagram.png" alt="drawing" width="800"/>




### Installation
We tested the code on python 3.8.10; Pytroch version '2.1.1+cu121'; GPU model GeForce RTX-4090.
```shell
conda env create -f environment.yml
conda activate lepard
cd cpp_wrappers; sh compile_wrappers.sh; cd ..
```





### Train and evaluation on 4DMatch
Download and extract the 4DMatch split to your custom folder. Then update the ```data_root``` in [configs/train/4dmatch.yaml](configs/train/4dmatch.yaml) and [configs/test/4dmatch.yaml](configs/test/4dmatch.yaml)


- Evaluate pre-trained
```shell
python main.py configs/test/4dmatch.yaml
```
(To switch between 4DMatch and 4DLoMatch benchmark, modify the ```split``` configuration in  [configs/test/4dmatch.yaml](configs/test/4dmatch.yaml))


- Train from scratch
```shell
python main.py configs/train/4dmatch.yaml
```


### Train and evaluation on 3DMatch
Download and extract the 3DMatch split to your custom folder. Then update the ```data_root``` in [configs/train/3dmatch.yaml](configs/train/3dmatch.yaml) and [configs/test/3dmatch.yaml](configs/test/3dmatch.yaml)

- Evaluate pre-trained
```shell
python main.py configs/test/3dmatch.yaml
```
(To switch between 3DMatch and 3DLoMatch benchmark, modify the ```split``` configuration in  [configs/test/3dmatch.yaml](configs/test/3dmatch.yaml))


- Train from scratch
```shell
python main.py configs/train/3dmatch.yaml
```

```text

```
