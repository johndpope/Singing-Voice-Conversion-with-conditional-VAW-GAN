# Singing-Voice-Conversion-with-conditional-VAW-GAN
This is the implementation of the paper "VAW-GAN for Singing Voice Conversion with Non-parallel Training Data". This work is submitted to APSIPA 2020.

## This work is about ...
In this work, we propose a singing voice conversion framework that is based on VAW-GAN [1]. We train an encoder to disentangle singer identity and singing prosody (F0 contour) from phonetic content. By conditioning on singer identity and F0, the decoder generates output spectral features with unseen target singer identity, and improves the F0 rendering. Our proposed method can significantly reduce the spectrum distortion and improve the converted singing quality. For more details, please refer to our paper.

## Getting Started


### Prerequisites

- Ubuntu 16.04  
- Python 3.6 
  - Tensorflow-gpu 1.5.0
  - PyWorld
  - librosa
  - soundfile
  - numpy 1.14.0
  - sklearn
  - glob
  - scipy
<br/>

### Database

In this work, we use  NUS  Sung  and  Spoken  Lyrics  Corpus (NUS-48E corpus) [2], which consists of the sung and spoken lyrics  of  48  English  songs  by  12  professional  singers.  We choose  two  male  singers  and  one  female  singers  for  all  the experiments.  For  each  singer,  6  songs  are  used  for  training and evaluation.<br/>

Please make sure your singing data is saved in the following structure and change the path in .json file:<br/>
"./data_multi/wav/training_set/SOURCE_SINGERID/xxxx.wav"<br/>
"./data_multi/wav/evaluation_set/TARGET_SINGERID/xxxx.wav"

## Usage
1. **Activate your virtual enviroment.**
```bash
source activate [your env]
```
2. **Extract features from raw audio.**
```Bash
$ python analyzer.py 
```
3. **Analyze features.**
```Bash
$ python build.py 
```
4. **Train the network.**
```Bash
$ python main-vawgan.py 
```
5. **Conversion.**
```Bash
$ python convert-vawgan.py --src 'SOURCE_SINGER_ID' --trg 'TARGET_SINGER_ID' --checkpoint './logdir/train/PLEASE_SPECIFY_YOUR_CHECKPOINT/model.ckpt-46860'
```
## References
[1] Hsu, Chin-Cheng, et al. "Voice conversion from unaligned corpora using variational autoencoding wasserstein generative adversarial networks." arXiv preprint arXiv:1704.00849 (2017). </br>
[2] Z. Duan, H. Fang, B. Li, K. Chai Sim, and Y. Wang, “The nus sung and spoken lyrics corpus: A quantitative comparison of singing and speech,”APSIPA, 2013

## Notes
1. The codes are based on VAW-GAN Voice Conversion: https://github.com/JeremyCCHsu/vae-npvc/tree/vawgan
2. Please feel free to contact me via my email: zhoukun@u.nus.edu if you are interested in our work.
