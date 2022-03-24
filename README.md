# Speaking-rate-controllable HiFi-GAN using Feature Interpolation

### Detai Xin Shinnosuke Takamichi, Takuma Okamoto, Hisashi Kawai, Hiroshi Saruwatari

This repo contains code for our paper  submitted to Interspeech 2022, which is a speaking-rate-controllable HiFi-GAN using feature inerpolation.

## Speaking rate control
1. See `README_hifi-gan.md` to install requirements and download pretrained HiFi-GAN model.
2. Changing speaking rate by the following cmd:
```shell
python3 inference.py --checkpoint_file /path/to/pretrained/generator --input_wavs_dir /path/to/wav/dir --method [linear|kaiser] --factor [speaking rate control factor] --layer [feature interpolation layer]
```
The generated wavs will be saved in `generated_files` by default.

## NICT-SpeedSpeech Dataset
You can also use our NICT-SpeedSpeech dataset to do your own experiments.
This dataset contains three kinds of speaking rate (slow, normal, fast) with 324 parallel utterances of two speakers (female, male).

[NICT-SpeedSpeech](https://ast-astrec.nict.go.jp/release/speedspeech_ja_2022/download.html)


## LICENCE
MIT