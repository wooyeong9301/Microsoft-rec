# Microsoft-rec
Microsoft Recommender Copy
- https://github.com/microsoft/recommenders   

### Versions
`Python` `Pytorch` `Anaconda` `Jupyter notebook`   
`Python 3.7.13` `cuda 11.2` `cudnn 8.1`   

```
conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1
conda install -c conda-forge pyspark
conda install pytorch torchvision torchaudio cudatoolkit=11.2 -c pytorch
```

```
pip install recommenders[examples,gpu,spark]
```   



22.07.22.
`import cornac`에서 오류가 있었습니다.
> Importerror libpython3.7m.so.1.0 cannot open shared object file no such file or director

정확한 이유는 잘 모르겠지만, Ubuntu 20.04버전의 기본 Python은 3.8버전인데,
현재 작업중인 가상환경의 Python은 3.7버전이어서 생기는 오류인 듯 합니다.
작업을 시작할 때마다 터미널에서 가상환경에 진입하여
> export LD_LIBRARY_PATH=/home/qwer/anaconda3/envs/recommender3713/lib
를 입력해 임시해결.
