# **Shono**: Bengali Speech Recognition

**Abstract**: This code implements an Automatic Speech Recognition (ASR) system for Bengali audio in [Bengali.AI Speech Recognition](https://www.kaggle.com/competitions/bengaliai-speech). The code uses a pre-trained Wav2Vec2 model (wav2vec2-large-mms-1b-bengali) for converting Bengali speech to text. It first loads various required packages and sets up a CTC (Connectionist Temporal Classification) decoder with a 5-gram language model for improving transcription accuracy. The pipeline processes test audio files by loading them using librosa, converting them to the required sampling rate (16kHz), and passing them through the Wav2Vec2 model to get logits. These logits are then decoded using beam search (with a beam width of 512) to generate text transcriptions. Finally, the text undergoes post-processing using a Bengali Unicode normalizer that handles proper formatting of Bengali text, including adding appropriate punctuation marks. The results are saved in a submission file with audio IDs and their corresponding transcribed sentences.

## Description
### Goal of the Competition
The goal of this competition is to recognize Bengali speech from out-of-distribution audio recordings. You will build a model trained on the first Massively Crowdsourced (MaCro) Bengali speech dataset with 1,200 hours of data from ~24,000 people from India and Bangladesh. The test set contains samples from 17 different domains that are not present in training.

### Context

![image](https://github.com/user-attachments/assets/502d4c20-fd78-41d6-8665-0e9729c0ea19)

Bengali is one of the most spoken languages in the world, with approximately 340 million native and second-language speakers globally. With that comes diversity in dialects and prosodic features (combinations of sounds). For example, Muslim religious sermons in Bengali are often delivered with a pace and tonality that is significantly different from regular speech. Such ‘shifts’ can be challenging even for commercially available speech recognition methods (the Google Speech API for Bengali has a Word Error Rate of 74% for Bengali religious sermons).

There are no robust open-source speech recognition models for Bengali currently, though your data science skills could certainly help change that. In particular, out-of-distribution generalization is a common machine learning problem. When test and training data are similar, they’re in-distribution. To account for Bengali’s diversity, this competition’s data is intentionally out-of-distribution, with the challenge to improve results.

Competition host Bengali.AI is a non-profit community initiative working to accelerate language technology research for Bengali (known locally as Bangla). Bengali.AI crowdsources large-scale datasets through community-driven collection campaigns and crowdsource solutions for their datasets through research competitions. All the outcomes from Bengali.AI's two-pronged approach, including datasets and trained models, are open-sourced for public use.
