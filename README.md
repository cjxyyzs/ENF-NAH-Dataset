# ENF-WHU-v2
This repository is dedicated to the ENF-WHU-v2 Dataset, an Electric Network Frequency (ENF) audio dataset collected around **Wuhan University** under unconstrained scenarios. It presents significant challenges to signal processing algorithms by complex and unconstrained real-world environments, where the weakness and partial absence of ENF signals along with environmental noise interference are prevalent. Additionally, it tests the impact of various recording devices on the ability to capture ENF signals, thereby increasing the complexity of analysis and application in broader and more practical scenarios.

- **Recording location**: coffee shops, KTVs, cinemas, parking lots, squares, parks, *etc.*, totaling more than ten different scenes.
- **Environment diversity**: day/night, rainy/sunny, interior/exterior.
- **Recording device**: Redmi K40, Aigo R6633, iPad Air4, Tascam DR-07x, Philips VTR7100, iPhone 13, *etc.*, totaling ten different devices.
- **Duration**: 5~30 minutes
- **Format**: PCM WAVE
- **Quantization depth**: 16-bit
- **Channel**: mono
- **Sampling frequency**: 8000 Hz (400 Hz for reference data)
- **Category**:
  - **'H1'**: "001~213.wav" 213 real-world recordings with captured ENF (noisy).
  - **'H1_ref'**: "001_ref~213_ref.wav" the corresponding 213 reference ENF (noise-free, same duration) obtained from power main.
  - **'H1_ref_one_day'**: the corresponding one-day (24 hours) reference ENF for the 213 recordings. "3-5,23.wav" means "003.wav", "004.wav", "005.wav" and "023.wav" in 'H1' folder are recorded within the same day.
  - **'H0'**: "001~027.wav" 27 real-world recordings without captured ENF.
# Note about the Ground-Truth 
The ground-truth matched location (the lag that corresponds to the true timestamp) can be determined by aligning noise-free reference files with their respective one-day references. For instance, matching "005_ref.wav" in 'H1_ref' folder with "3-5,23.wav" in 'H1_ref_one_day' folder yields the lag index, serving as the ground truth timestamp for "005.wav" in 'H1' folder. This implies that "005.wav" should align with the same or very close lag index in "3-5,23.wav". Correlation coefficient (CC) can be used for the matching criterion as long as the recording and reference are matched using the same criterion.

# Recording Information
## Environment
The ENF-WHU-v2 dataset expands beyond the original campus-based recordings of the [ENF-WHU dataset](https://github.com/ghua-ac/ENF-WHU-Dataset) to include over ten diverse scenes such as cafes, KTVs, cinemas, and parks, embracing both indoor and outdoor settings across different times. This strategic selection aims to more accurately mirror real-life forensic scenarios, ranging from quiet indoor environments to complex outdoor locations with varying ENF signal strengths due to factors like AC electrical activities and infrastructure. 

## Devices
The ENF-WHU-v2 dataset, detailed in the following table, is compiled from audio captures recorded using a variety of widely-used devices, including smartphones, laptops, tablets, and digital voice recorders. This diverse collection serves as a valuable resource for investigating how different types of recording devices affect the fidelity of ENF signals. Notably, by exclusively using battery power for recordings, the dataset ensures an environment free from AC power interference, maintaining 'device-unconstrained' conditions that mirror real-life scenarios.
<div align="center">
<table>
  <tr>
    <th align="center">Device Type</th>
    <th align="center">Brand and Model</th>
    <th align="center">Operating System</th>
    <th align="center">Default Recording Format</th>
  </tr>
  <tr>
    <td align="center">Smartphone</td>
    <td align="center">iPhone 13</td>
    <td align="center">iOS 15.6.1</td>
    <td align="center">M4A</td>
  </tr>
  <tr>
    <td align="center">Smartphone</td>
    <td align="center">Redmi K40</td>
    <td align="center">MIUI 14.0.6</td>
    <td align="center">WAV</td>
  </tr>
  <tr>
    <td align="center">Smartphone</td>
    <td align="center">HUAWEI nova</td>
    <td align="center">Android 13.0</td>
    <td align="center">M4A</td>
  </tr>
  <tr>
    <td align="center">Tablet</td>
    <td align="center">iPad Air 4</td>
    <td align="center">iPadOS 15.6.1</td>
    <td align="center">M4A</td>
  </tr>
  <tr>
    <td align="center">Tablet</td>
    <td align="center">HUAWEI MatePad 11</td>
    <td align="center">HarmonyOS 2.0</td>
    <td align="center">M4A</td>
  </tr>
  <tr>
    <td align="center">Laptop</td>
    <td align="center">MacBook Air 2017</td>
    <td align="center">macOS Monterey 12.6.3</td>
    <td align="center">M4A</td>
  </tr>
  <tr>
    <td align="center">Laptop</td>
    <td align="center">HONOR MagicBook</td>
    <td align="center">Windows 10</td>
    <td align="center">M4A</td>
  </tr>
  <tr>
    <td align="center">Voice Recorder</td>
    <td align="center">Aigo R6633</td>
    <td align="center">——</td>
    <td align="center">WAV</td>
  </tr>
  <tr>
    <td align="center">Voice Recorder</td>
    <td align="center">Philips VTR7100</td>
    <td align="center">——</td>
    <td align="center">WAV</td>
  </tr>
  <tr>
    <td align="center">Voice Recorder</td>
    <td align="center">TASCAM DR-07X</td>
    <td align="center">——</td>
    <td align="center">WAV</td>
  </tr>
</table>
</div>

## Duration
The ENF-WHU-v2 dataset's audio durations are tailored based on an analysis of needs across various ENF forensic studies, ensuring versatility for different research objectives. Durations range from one to over forty minutes for timestamp verification, while tampering detection focuses on clips between nineteen seconds to twenty minutes. ENF signal estimation requires two to fifty minutes of audio to analyze grid frequency features accurately. Video forensics with ENF spans from short one-minute to longer recordings. The dataset's five to thirty-minute recordings strike a balance, covering a wide spectrum of forensic analysis scenarios.


# Citation Information
- **Tampering Detection**:
  



