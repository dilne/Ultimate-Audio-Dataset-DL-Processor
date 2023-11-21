<h1 align="center">📊Ultimate Audio Dataset DL Processor🔊</h1>

<a href="https://colab.research.google.com/github/dilne/Ultimate-Audio-Dataset-DL-Processor/blob/main/Ultimate%20Audio%20Dataset%20DL%20Processor.ipynb" target="_blank">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

This repository uses librosa to load audio, prints its core features, display in a variety of formats, and convert (including batch convert) to different formats.

## Display the waveform
A waveform serves as a fundamental visual depiction of an audio signal, illustrating the fluctuation of amplitude over a period of time. The graph plots time along the horizontal (X) axis and amplitude on the vertical (Y) axis. However, it’s important to note that while it provides a snapshot of amplitude variations, it doesn’t offer insights into frequency changes.

![alt text](https://github.com/dilne/Ultimate-Audio-Dataset-DL-Processor/blob/main/Images/Waveform.png "Waveform Example")

## Display the spectogram
A spectrogram offers a comprehensive visual representation of an audio signal, encapsulating all three fundamental characteristics of sound. The horizontal (X) axis denotes time, the vertical (Y) axis represents frequencies, and the color spectrum signifies amplitude. This three-dimensional graph provides a convenient way to monitor frequency changes over time, explore the richness of the sound, and visually identify potential issues such as noise or patterns. It’s a powerful tool for in-depth audio analysis.

![alt text](https://github.com/dilne/Ultimate-Audio-Dataset-DL-Processor/blob/main/Images/Spectogram.png "Spectogram Example")

## Display the mel spectogram
A Mel spectrogram, named after the Mel scale (after the word melody), is a type of spectrogram that applies perceptual weighting to better reflect human hearing. The mel scale is a perceptual scale of pitches judged by listeners to be equal in distance from one another. The reference point between this scale and normal frequency measurement is defined by assigning a perceptual pitch of 1000 mels to a 1000 Hz tone, 40 dB above the listener’s threshold.

The human ear is more sensitive to lower frequencies than higher ones, and the mel scale accounts for this by compressing the frequency scale in a way that approximates the human auditory system’s response. In a Mel spectrogram, frequency values in Hertz are converted into the mel scale, providing a more perceptually relevant representation.

Mel spectrograms are widely used in various audio signal processing tasks. These include genre classification, where different musical genres often exhibit distinct patterns in the mel spectrogram; instrument detection in songs, where different instruments can produce unique spectral shapes; and speech emotion recognition, where the mel spectrogram can capture the prosodic (properties of syllables and larger units of speech, including linguistic functions such as intonation, stress, and rhythm) and spectral variations associated with different emotional states.

![alt text](https://github.com/dilne/Ultimate-Audio-Dataset-DL-Processor/blob/main/Images/Mel%20spectogram.png "Mel Spectogram Example")

## Display the mel frequency cepstral coefficient (MFCC)
Mel Frequency Cepstral Coefficients (MFCCs) are a widely used feature in audio signal processing, particularly for speech recognition and music information retrieval. They provide a compact representation of the spectral envelope of an audio signal.

The MFCCs are derived from the Mel-frequency cepstrum (MFC), which is a representation of the short-term power spectrum of a sound. The MFC is based on a linear cosine transform of a log power spectrum on a nonlinear Mel scale of frequency.

The process of calculating MFCCs involves several steps:

1. The audio signal is first divided into short frames.
2. The power spectrum of each frame is calculated using the Fast Fourier Transform (FFT).
3. The power spectrum is then mapped onto the Mel scale using a set of overlapping triangular filters.
4. The log of the power in each Mel frequency band is taken.
5. The Discrete Cosine Transform (DCT) of the list of log powers is taken.
6. The MFCCs are the amplitudes of the resulting spectrum.

The MFCCs provide a robust and efficient representation of the spectral shape of an audio signal, making them a powerful tool for tasks such as genre classification, instrument detection in songs, and speech emotion recognition.

![alt text](https://github.com/dilne/Ultimate-Audio-Dataset-DL-Processor/blob/main/Images/MFCC.png "MFCC Example")

## Display the chromagram
A chromagram is a representation of an audio signal that displays how the intensity of different pitches changes over time. It is closely related to the twelve different pitch classes in Western music.

The term “chroma” refers to the perceived color, or quality, of a musical note. In a chromagram, each of the twelve pitch classes (C, C♯, D, D♯, E, F, F♯, G, G♯, A, A♯, B) is assigned a unique chroma. The chromagram then shows how the intensity of each chroma changes over time.

One of the key properties of chroma features is that they capture the harmonic and melodic characteristics of music, while being robust to changes in timbre and instrumentation. This makes chromagrams a powerful tool for analyzing music, as they allow you to see how the harmonic content of the music changes over time.

To create a chromagram, the audio signal is first divided into short frames. For each frame, the power spectrum is calculated, and this spectrum is then mapped onto the twelve chroma bands. The resulting time-chroma representation is the chromagram.

Chromagrams are used in a variety of applications, including chord recognition, genre classification, and music recommendation. They are particularly useful for tasks that involve identifying pitches that differ by an octave, as they are robust to variations in timbre.

![alt text](https://github.com/dilne/Ultimate-Audio-Dataset-DL-Processor/blob/main/Images/Chromagram.png "Chromagram Example")

## Display the fast fourier transform (FFT)
The Fast Fourier Transform (FFT) is a crucial tool in the field of audio and acoustics measurement. It works by converting a signal into individual spectral components, thereby providing frequency information about the signal. The FFT is essentially an optimized algorithm for the implementation of the Discrete Fourier Transformation (DFT), where a signal is sampled over a period of time and divided into its frequency components. These components are single sinusoidal oscillations at distinct frequencies each with their own amplitude and phase. The FFT is used for fault analysis, quality control, and condition monitoring of machines or systems.

![alt text](https://github.com/dilne/Ultimate-Audio-Dataset-DL-Processor/blob/main/Images/FFT.png "FFT Example")

## Display the Short-time fast fourier transform (STFT)
The Short-Time Fourier Transform (STFT) is another powerful tool for audio signal processing. It defines a particularly useful class of time-frequency distributions which specify complex amplitude versus time and frequency for any signal. The STFT is used to determine the sinusoidal frequency and phase content of local sections of a signal as it changes over time. In practice, the procedure for computing STFTs is to divide a longer time signal into shorter segments of equal length and then compute the Fourier transform separately on each shorter segment. This reveals the Fourier spectrum on each shorter segment.

![alt text](https://github.com/dilne/Ultimate-Audio-Dataset-DL-Processor/blob/main/Images/STFT.png "STFT Example")
