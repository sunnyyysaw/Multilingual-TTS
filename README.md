# Multilingual-TTS (Text-to-Speech) System Using Suno’s Bark Model
## Overview

This project presents a multilingual Text-to-Speech (TTS) system built on Suno AI’s Bark model, a transformer-based architecture capable of producing natural, expressive speech across various languages and speaker profiles. The system is designed to overcome limitations in traditional TTS systems, such as robotic-sounding output, limited language support, and lack of voice diversity.

## Key Features

Multilingual Support: Supports a wide range of languages including English, Hindi, Chinese, French, German, Italian, Polish, and more.

Speaker Variety: Offers both male and female voice options with support for conditional speaker embeddings to customize voice tone and identity.

Realistic Output: Capable of generating not just speech, but non-verbal expressions like sighs, laughs, background sounds, and emotional tone.

Efficient Inference: Implements CPU offloading and half-precision computing for faster real-time generation.

## System Architecture

The system processes text input through a series of components to generate high-quality speech:

Text Input: User-provided text to be synthesized.

Text Preprocessing:

- Normalization: Lowercasing, punctuation removal, special character handling.

- Tokenization: Splits text into processable units.

- Text Cleaning (optional): Custom rules for typos, abbreviations, and formatting.

![image](https://github.com/user-attachments/assets/2f0d5f05-158a-4e21-b2af-9e2174167d8a)

Text Encoder: Uses a transformer model to convert text into a meaningful numerical representation.

Mel Spectrogram Decoder: Predicts a mel spectrogram, capturing acoustic characteristics of human speech.

Vocoder: Converts the spectrogram into a final audio waveform. Users can choose from different vocoder options based on quality/speed.

Audio Post-Processing (optional):

- Volume Normalization

- Noise Reduction

Final Output: Synthesized speech can be played or saved as a WAV file.

## Bark Model Components

BarkSemanticModel: Predicts semantic tokens from the input text.

BarkCoarseModel: Generates the first set of audio codebooks based on semantic tokens.

BarkFineModel: Refines and completes the audio representation using additional codebooks.

EncodecModel: Decodes the final codebooks into natural-sounding audio.

## Workflow Steps

Utilizes Python libraries like torch, transformers, torchaudio, numpy, and matplotlib.

Load the processor and model using AutoProcessor and AutoModel.

Split input text into manageable sentences.

Process each sentence and run inference to generate audio samples.

Apply post-processing (e.g., noise filtering, amplitude thresholding).

Concatenate audio outputs into a single audio file.

Save output as a WAV file or NumPy array.

Visualize waveform and amplitude using matplotlib.

## Performance Evaluation

Processing time per sentence

Rolling amplitude trends

Audio quality (clarity, fluency, naturalness)

## Conclusion

We successfully built a reliable Multilingual Text-to-Speech system using the Bark model, supporting multiple languages like Hindi, English, Chinese, Italian, French, German, and Polish. The system features male and female voices, handles various acoustic conditions, and produces natural-sounding speech. Extensive testing confirmed its efficiency, adaptability, and user inclusivity, making it ideal for diverse real-world applications.
