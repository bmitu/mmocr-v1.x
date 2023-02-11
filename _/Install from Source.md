# Install from Source

Last verified at 2023/02/10

```shell
wget https://repo.anaconda.com/miniconda/Miniconda3-py38_23.1.0-1-Linux-x86_64.sh
bash Miniconda3-*

conda create --name openmmlab python=3.8 -y
conda activate openmmlab

conda install pytorch torchvision -c pytorch -y

pip install -U openmim
mim install mmengine
mim install 'mmcv>=2.0.0rc1'

pip install 'mmdet>=3.0.0rc0'

cd ..mmocr-v1.x
git checkout dev-1.x

pip install -r requirements.txt
pip install -v -e .

python mmocr/ocr.py --det DB_r18 --rec CRNN --print-result --img-out-dir _/output demo/demo_text_ocr.jpg 
```

Works with some warnings (seemingly minor)
