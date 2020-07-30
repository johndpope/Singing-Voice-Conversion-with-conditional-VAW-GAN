# Singing-Voice-Conversion-with-conditional-VAW-GAN
This is the implementation of the paper "VAW-GAN for Singing Voice Conversion with Non-parallel Training Data". This work is submitted to APSIPA 2020.

## This work is about ...
In this work, we propose a singing voice conversion framework that is based on VAW-GAN. We train an encoder to disentangle singer identity and singing prosody (F0 contour) from phonetic content. By conditioning on singer identity and F0, the decoder generates output spectral features with unseen target singer identity, and improves the F0 rendering. Our proposed can significantly reduce the spectrum distortion and improve the converted sining quality. For more details, please refer to our paper.

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

## Usage
1. **Activate your virtual enviroment.**
```bash
source activate [your env]
```
