# Singing-Voice-Conversion-with-conditional-VAW-GAN
This is the implementation of the paper "VAW-GAN for Singing Voice Conversion with Non-parallel Training Data". This work is submitted to APSIPA 2020.

## This work is about ...
In this work, we propose a singing voice conversion framework that is based on VAW-GAN [1]. We train an encoder to disentangle singer identity and singing prosody (F0 contour) from phonetic content. By conditioning on singer identity and F0, the decoder generates output spectral features with unseen target singer identity, and improves the F0 rendering. Our proposed can significantly reduce the spectrum distortion and improve the converted sining quality. For more details, please refer to our paper.

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
In this work, we use  NUS  Sung  and  Spoken  Lyrics  Corpus (NUS-48E corpus) [2], which consists of the sung and spoken lyrics  of  48  English  songs  by  12  professional  singers.  We choose  two  male  singers  and  one  female  singers  for  all  the experiments.  For  each  singer,  6  songs  are  used  for  training and evaluation.

Please make sure your singing data is saved in the following structure:<br/>
"./data_multi/wav/training_data/SINGERID/xxxx.wav"<br/>
"./data_multi/wav/evaluation_data/SINGERID/xxxx.wav"

## Usage
1. **Activate your virtual enviroment.**
```bash
source activate [your env]
```
2. **Extract features from raw audio.**
3. **Train the network.**
4. **Conversion.**

## References
[1] Hsu, Chin-Cheng, et al. "Voice conversion from unaligned corpora using variational autoencoding wasserstein generative adversarial networks." arXiv preprint arXiv:1704.00849 (2017).
[2] Z. Duan, H. Fang, B. Li, K. Chai Sim, and Y. Wang, “The nus sung andspoken lyrics corpus: A quantitative comparison of singing and speech,”APSIPA, 2013
