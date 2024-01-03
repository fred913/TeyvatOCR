# Intro

This project is implemented based on [EasyOCR](https://github.com/JaidedAI/EasyOCR) and [ABINet](https://github.com/FangShancheng/ABINet), where EasyOCR recognizes the file and locates the frame and ABINet recognizes the text content.

Dataset is generated from [Teyvat Font by 采薇东篱夏](https://bbs.mihoyo.com/ys/article/9058992) on hoYoLabs, using [TextRecognitionDataGenerator](https://github.com/Belval/TextRecognitionDataGenerator).
The [albumentations](https://albumentations.readthedocs.io/) library is used for data augmentation during the dataset generation process to improve the model's generalization ability.

# Dataset Generation

Run:
```bash
cd data_gen
python text_gen.py
```
Generate the dataset you want, and install whatever library you need.

# Install Requirements

```bash
pip install -r requirements.txt
```

# Usage

You may download the pretrained model from the netdisk link.
Baidu Netdisk (for China (Mainland) users): https://pan.baidu.com/s/1TrXBIybAO6-WmXHzzn0krw 
Passcode: e3ah

Put it into the ABINet folder.

Image OCR
```bash
python demo_image.py -p <input file path>
python demo_image.py -p <input file path> --step # with the process video
```

Video OCR
```bash
python demo_video.py -p <input file path>
```

![Model Evalution](image/kl.png)
