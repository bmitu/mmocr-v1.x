# MMOCR v1.x Journal

## 2023/02/09

- Forked mmocr: <https://github.com/bmitu/mmocr-v1.x>
- Used branch `dev-1.x`
- Tried to use mmocr in docker container; didn't work
- Installed mmocr from source.
- Run OCR demo with warnings:
    - The "model" registry in mmdet did not set import location.
    Warning can be ignored (see https://github.com/open-mmlab/mmdetection/discussions/9548)
    - The model and loaded state dict do not match exactly 
      unexpected key in source state_dict: data_preprocessor.mean, data_preprocessor.std
- Run again in docker, worked with warnings after after changing arg from --rec to --recog

NOTE: Model conversion is now done with `mmdeploy`
