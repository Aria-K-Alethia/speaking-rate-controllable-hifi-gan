# Speaking-rate-controllable HiFi-GAN using Feature Interpolation

### Detai Xin Shinnosuke Takamichi, Takuma Okamoto, Hisashi Kawai, Hiroshi Saruwatari

**Abstract**:This paper presents a speaking-rate-controllable HiFi-GAN neural vocoder.
Original HiFi-GAN is a high-fidelity, computationally efficient, and tiny-footprint neural vocoder.
We attempt to incorporate a speaking rate control function into HiFi-GAN for improving the accessibility of synthetic speech.
The proposed method inserts a differentiable interpolation layer into the HiFi-GAN architecture.
A signal resampling method and an image scaling method are implemented in the proposed method to warp the mel-spectrograms or hidden features of the neural vocoder.
We also design and open-source a Japanese speech corpus containing three kinds of speaking rates to evaluate the proposed speaking rate control method.
Experimental results of comprehensive objective and subjective evaluations demonstrate that 1) the proposed method outperforms a baseline time-scale modification algorithm in speech naturalness, 2) warping mel-spectrograms by image scaling obtained the best performance among all proposed methods, and 3) the proposed speaking rate control method can be incorporated into HiFi-GAN without losing computational efficiency.

This repo contains code for our paper  submitted to Interspeech 2022, which is a speaking-rate-controllable HiFi-GAN using feature inerpolation.

## Speaking rate control
1. See `README_hifi-gan.md` to install requirements and download pretrained HiFi-GAN model.
2. Changing speaking rate by the following cmd:
```shell
python3 inference.py --checkpoint_file /path/to/pretrained/generator --input_wavs_dir /path/to/wav/dir --method [linear|kaiser] --factor [speaking rate control factor] --layer [feature interpolation layer]
```
The generated wavs will be saved in `generated_files` by default.

## NICT-SpeedSpeech-JA-2022 Dataset
You can also use our NICT-SpeedSpeech-JA-2022  dataset to do your own experiments.
This dataset contains three kinds of speaking rate (slow, normal, fast) with 324 parallel utterances of two speakers (female, male).

[NICT-SpeedSpeech](https://ast-astrec.nict.go.jp/release/speedspeech_ja_2022/download.html)


## LICENCE
MIT
