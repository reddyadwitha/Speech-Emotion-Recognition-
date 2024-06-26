# Speech-Emotion-Recognition-
This project explores speech emotion recognition using the RAVDESS dataset. It investigates the effectiveness of spectrograms, chromagrams, data augmentation techniques (specAugment and additive white Gaussian noise), and different CNN architectures for classifying emotional states in audio files.

Dataset

The RAVDESS dataset is used, containing audio recordings of various emotions (neutral, calm, happy, sad, angry, fearful, surprised, disgusted) expressed by professional actors.
Data Preprocessing

Spectrogram Generation:

Audio files are converted into spectrograms, which represent the frequency content of the audio signal over time.
Libraries like Librosa or torchaudio can be used for this purpose.
Chromagram Generation:

Chromagrams capture the tonal content of the audio signal, focusing on the presence of specific pitches.
Similar libraries can be employed to create chromagrams.
Data Augmentation:

SpecAugment is applied to spectrograms to introduce controlled variations in time, frequency, and mask domain, enhancing model robustness.
Additive white Gaussian noise is added to chromagrams at a low level to make the model less sensitive to noise present in real-world data.
Model Architectures

1. CNN for Spectrograms:
A convolutional neural network (CNN) architecture specifically designed for analyzing spectrograms is implemented.
The CNN model captures spatial relationships within the spectrogram image, potentially identifying patterns indicative of emotion.

2. CNN for Chromagrams:
A separate CNN architecture tailored for chromagrams is created.
This model can learn from the pitch information encoded in the chromagram to differentiate emotions.

3. CNN with Fused Features:
Features extracted from both spectrograms and chromagrams are concatenated and fed into a single CNN model.
This approach aims to leverage the complementary information from both representations, potentially leading to improved recognition accuracy.
