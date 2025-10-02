# SecureVoice50-A-Multi-Device-Multi-Environment-Speech-Dataset-for-Secure-Speaker-Verification

## Abstract

This paper introduces a speech dataset developed to advance research in speaker identification and voice biometric verification, particularly in the context of mobile banking and other security-sensitive applications. 

The dataset comprises recordings from 50 participants with diverse linguistic and cultural backgrounds and varying levels of English proficiency. 

Each participant provided voice samples across multiple devices, including low-end smartphones, in-call scenarios, and external microphones, recorded in both indoor and outdoor environments to reflect real-world usage conditions. 

The corpus is organized into anonymized speaker folders containing .wav files, complemented by a metadata file with non-identifiable demographic attributes. 

Unlike existing datasets that primarily target recognition accuracy under clean conditions, this resource was specifically designed to support security-oriented studies, including degradation-aware evaluation, spoofing resilience, liveness detection, and adaptive verification mechanisms. 

This dataset represents one of the first corpora tailored for secure mobile banking on low-end devices. Its multi-device, multi-environment design enables robustness evaluation under real-world conditions such as environmental noise, channel distortion, and spoofing attempts, offering a reproducible and scalable foundation for advancing research in secure voice biometric systems. 

## Experiment Design
# Participants

The dataset was collected from 50 participants at the Nara Institute of Science and Technology (NAIST), consisting of 20 female and 30 male speakers aged between 21 and 38 years. 

Participants were recruited from Africa, Asia, and Europe, ensuring a mix of linguistic and cultural backgrounds. English proficiency was self-reported as advanced (23 participants), intermediate (22 participants), and basic (5 participants). 

Each participant was asked to read 50 distinct English phrases sourced from the IEEE Top Tech 2023 magazine, chosen for their phonetic diversity and variability in speech content.

## Device 

Gratina 4G (OS v5.1.1): A Japanese low-end feature phone widely available in developing markets. It was chosen because its basic hardware and narrowband microphone capture the limitations of legacy devices still used for mobile banking transactions. This represents the minimum baseline for speech quality in such environments.

Gratina in-call setup: In addition to direct recordings, speech was captured during simulated phone calls using the same device to include the effects of voice compression, packet loss, and channel distortion introduced by cellular networks. This setup reflects the actual audio quality experienced when customers interact with call-based banking services.

Samsung A04s and Infinix HOT 8 (Android smartphones): These mid-range devices are representative of the most common smartphones in developing regions. They provide a balance between affordability and performance, allowing comparison of how different Android microphones and processing pipelines affect biometric verification.

iPhone SE: A higher-end smartphone with advanced audio processing and microphone arrays. This device was included to serve as a contrast to the lower-end Android phones and to capture data from premium consumer hardware frequently used in developed regions.

External microphone on MacBook: A USB condenser microphone connected to a MacBook provided high-quality reference recordings. This channel represents near-studio quality audio, serving as an upper benchmark against which the effects of device and network degradation can be measured.

## Value of the Data 
- Further validation was conducted using a speaker identification system trained on embeddings extracted with Whisper and ECAPA models. 

- Verification performance was measured with cosine similarity, angular distance, Equal Error Rate (EER), and ROC curves. 

- Over 100 training epochs, the system demonstrated consistent generalization, with the loss decreasing from 0.1654 to 0.0412. 

### Environments
Two environments were included to simulate real-world usage:
- Indoor recordings: Collected in the NAIST Building A lobby, a semi-controlled environment with background activity such as footsteps and conversations.
- Outdoor recordings: Captured in campus surroundings, incorporating natural noise sources such as wind, traffic, and crowd movement.


### Audio files (.wav)
- 12 anonymized speaker folders (`speaker_01`, `speaker_02`, …)  
- Each folder contains ~40 utterances  
- Sampling rates: **8–16 kHz**, 16-bit PCM  
- File naming: `audio_1.wav`, `audio_2.wav`, …

  
**Data Format**
- The main fields per entry in the dataset are: **Participant ID, Nationality, English Proficiency, Age, Gender, Status**.
- The data is available in both **.csv** and **.JSON** formats. 

Below is an example of an entry from our dataset:
```
    {
        "participant_id":"ZVMKSJ",
        "nationality":"Indonesia",
        "english_proficiency":"Basic",
        "age":38.0,
        "gender":"Male",
        "status":"present"
    }
```
## License
This dataset is released under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.  
You are free to **use, share, and adapt** the dataset with appropriate attribution.  

## Download the Dataset
The dataset is available on **Hugging Face**:  
👉 (https://huggingface.co/datasets/Oye12/SecureVoice50)


---
## Citation
If you use this dataset, please cite the following:

```bibtex
@dataset{oyebode_securevoice50_2025,
  author       = {Oyebode, Oluwatobi},
  title        = {SecureVoice50: A Multi-Device, Multi-Environment Speech Dataset for Robust and Secure Speaker Verification},
  year         = {2025},
  publisher    = {Zenodo},
  version      = {v1.0.0},
  doi          = {10.5281/zenodo.17184012},
  url          = {https://doi.org/10.5281/zenodo.17184012}
}
```
