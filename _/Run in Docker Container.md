# Use MMOCR 1.x in Docker Container

## 2023/02/09: ~~didn't work.~~ worked with warnings after changing arg from --rec to --recog

```
The model and loaded state dict do not match exactly

unexpected key in source state_dict: data_preprocessor.mean, data_preprocessor.std
```

References:

- <https://mmocr.readthedocs.io/en/dev-1.x/get_started/install.html>

```shell
# build an image with PyTorch 1.6, CUDA 10.1
sudo docker build -t mmocr docker/

sudo docker run -it --gpus all --shm-size=8g -it -v /home/ubuntu/OpenMMLab/mmocr-v1.x:/host mmocr
```

python mmocr/ocr.py --det DB_r18 --recog CRNN --print-result --img-out-dir _/output demo/demo_text_ocr.jpg

--> works with warnings
