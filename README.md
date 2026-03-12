 <h1 align="center">
   COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM
    </h1>

## **Overview**
This is a laboratory report on Communication 2. In this report, viewers can see the input, process, and the output of each experiments. The theoretical explanation behind it will also be discussed and how to use each discipline pratically.    

## Table of Contents
* Part 1 - FM Modulation & Demodulation
* Part 2 - Sampling & Reconstruction
* Part 3 - PCM Encoding & Decoding
* Part 4 - Bandwidth Limiting and Restoring Digital Signals
* Summary 
* Learnings

## I - FM Modulation & Demodulation 
While DSBSC and SSB systems are vulnerable to electrical noise—which interferes with signal amplitude—Frequency Modulation (FM) is more robust. Because FM demodulators track frequency changes rather than amplitude, they ignore the noise-induced "spikes" that plague other systems.

### Modulation Mechanics
FM is generated using an oscillator with an adjustable frequency. The process follows these rules:
* Rest Frequency: The output when the input message is at $0V$.
* Deviation: As input voltage increases or decreases, the output frequency deviates proportionally from the center frequency.
* Flat Envelope: Unlike AM, the carrier’s amplitude remains constant, resulting in a flat signal envelope.

 <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5a7b8e464ac0cef854201cc690fa3e194cf0d7a0/Exp%209/modulator.png" alt="Modulator">

### Demodulation Methods
There are numerous ways to recover the original message from an FM signal, including:
* Slope detectors and Ratio detectors.
* Phase-locked loops (PLL).
* Zero-crossing detectors (the primary method used for introductory experiments).

### The Zero-Crossing Detector (ZCD)
The Zero-crossing Detector is an efficient method for FM demodulation. It operates by converting frequency variations into a measurable DC component.

 <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5a7b8e464ac0cef854201cc690fa3e194cf0d7a0/Exp%2010/demod.png" alt="Modulator">
  
  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5a7b8e464ac0cef854201cc690fa3e194cf0d7a0/Exp%2010/demod1.png" alt="Modulator">

Operating Principles:
1. Signal Conditioning: The received FM signal passes through a comparator, which heavily clips the waveform to produce a square wave trigger signal.
2. Frequency to Duty Cycle Conversion: As the FM signal’s frequency varies with the message, the frequency of the ZCD's rectangular output changes accordingly. Since the "mark" (pulse width) is fixed, these frequency shifts change the duty cycle (mark/space ratio).
3. DC Extraction: Because the average DC voltage of a pulse train is directly proportional to its duty cycle, the resulting DC component becomes a replica of the original modulating signal.
4. Low-Pass Filtering: A Low-Pass Filter (LPF) is used to extract this changing DC component, effectively recovering the original message, whether it is a sine wave or speech.

### FM Modulator & Demodulator Experiment equipment 
* Emona Telecom-Trainer 101 (plus power-pack)
* Dual Channel 20Mhz oscilloscope
* Two Emona Telecom-Trainer 101 oscilloscope leads
* Assorted Emona Telecom’s Trainer 101 patch leads
* One set of headphones (Sterio)


<details>
  <summary>RESULTS in FM Modulator</summary>

  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.1.jpg" alt="Modulator">
  $FM-Squarewave$
  
  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.2.jpg" alt="Modulator">
   $FM-Squarewave$
  
  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.3.jpg" alt="Modulator">
  $Min. VCO$
  
  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.4.jpg" alt="Modulator">
  $Mid. VCO$
  
  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.5.jpg" alt="Modulator">
  $Max. VCO$
  
  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.6.jpg" alt="Modulator">
  
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.7.jpg" alt="Modulator">
   $Without-voice$
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.8.jpg" alt="Modulator">
   $With-voice$
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.9.jpg" alt="Modulator">
   <i>With 10khz voice</i>
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.10.jpg" alt="Modulator">
   <i>with 5khz voice</i>
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.11.jpg" alt="Modulator">
   
 </details>


 <details>
  <summary>RESULTS in FM Demodulator</summary>

   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%2010/10-Part-A-1-FM.png" alt="Demodulator">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%2010/10-Part-B-1-FM-TP.png" alt="Demodulator">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%2010/10-Part-B-2-Message(red)-DemodulatedMessage(blue).png" alt="Demodulator">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%2010/10-Part-C-1-Fig10.png" alt="Demodulator">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%2010/10-Part-C-2-Fig12.png" alt="Demodulator">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%2010/10-Part-C-3-Fig14.png" alt="Demodulator">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%2010/10-Part-D-1-Fig16.png" alt="Demodulator">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%2010/10-Part-D-2-Fig18.png" alt="Demodulator">

   </details>


## II - Sampling and Reconstruction 
While modern communication increasingly relies on digital transmission for its superior noise resistance, analog messages (such as speech) must first be converted via sampling. This process involves measuring the analog signal's voltage at regular intervals using a digital sampling signal.

### Sampling Methods
* Natural Sampling: The sampled signal follows the analog message's voltage for the duration of the sampling pulse.
* Sample-and-Hold (PAM): The voltage is fixed at the instant of measurement, creating a "flat-top" pulse. This is often required for systems that cannot process fluctuating signal levels during a single sample.

<img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/23952d2782739c11364ed5e8dcec5f8bd32646ba/Exp%2011/sampling.png" alt="Sampling">

#### Mathematical Model and Recovery
Sampling is mathematically defined as the multiplication of the message signal by the sampling signal:

$$\text{Sampled Message} = (\text{DC} + \text{Fundamental} + \text{Harmonics}) \times \text{Message}$$

This multiplication creates a complex output consisting of the original message frequency, plus various sum and difference frequencies (sidebands) centered around the sampling frequency and its harmonics.

To recover the original message, the sampled signal is passed through a Low-Pass Filter (LPF). The filter rejects the high-frequency harmonics and sidebands, allowing only the original low-frequency message signal to pass through.
          
 ### Experiment Equipments 
 * Emona Telecom-Trainer 101 (plus power-pack)
 * Dual Channel 20Mhz oscilloscope
 * Two Emona Telecom-Trainer 101 oscilloscope leads
 *  Assorted Emona Telecom’s Trainer 101 patch leads
  
  <details>
  <summary>RESULTS</summary>

   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.1.jpg" alt="Sampling">
   <i>Without VDC</i>
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.2.jpg" alt="Sampling">
   <i>with VDC</i>
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.3.jpg" alt="Sampling">
 
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.4.jpg" alt="Sampling">

   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.5.jpg" alt="Sampling">

   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.6.jpg" alt="Sampling">
   <i>With direct voice</i>
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.7.jpg" alt="Sampling">
   <i>without direct voice</i>

   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.8.jpg" alt="Sampling">
   <i>cut off</i>

   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.9.jpg" alt="Sampling">
  
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.10.jpg" alt="Sampling">
   

   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.11.jpg" alt="Sampling">
 

  </details>


## III - PCM Encoding & Decoding
Pulse Code Modulation (PCM) is the standard method for converting analog signals into digital serial data. 

### PCM Encoding 
To convert an analog voltage into a binary stream, the encoder performs the following steps:
1. Sampling: Measuring the analog signal’s voltage at discrete time intervals.
2. Quantization: Comparing the sampled voltage to a set of fixed reference levels and selecting the nearest value.
3. Encoding: Assigning a unique binary number to the chosen quantization level and outputting it serially.

#### The accuracy of a PCM system depends on two critical parameters:
* Sampling Rate & Aliasing: To accurately reconstruct the signal, the sampling frequency must be at least twice the highest frequency of the message signal (the Nyquist Rate). Failure to meet this results in aliasing.
* Quantization Error: Since samples are rounded to the nearest quantization level, the original exact value is lost. This difference is known as quantization error. Increasing the number of levels reduces this error.

#### The Emona PCM Encoder uses an 8-bit codec with the following specifications:
* Voltage Range: $-2\text{V}$ to $+2\text{V}$.
* Resolution: 8 bits ($2^8$), providing 256 distinct quantization levels.
* Data Format: Bits are transmitted in frames, starting with the Most Significant Bit (bit-7) and ending with the Least Significant Bit (bit-0).
* Synchronization: The module generates a Frame Synchronization (FS) signal that pulses high during bit-0, allowing an oscilloscope to trigger and align the data frames correctly.

### PCM Decoding 
Decoding recovers the original analog message from a digital serial stream. On the Emona Telecoms-Trainer 101, the process involves several key stages to transform 8-bit data back into a continuous waveform.

#### The Decoding Sequence
* Frame Identification: Locating the start of each 8-bit packet in the serial stream.
* D/A Conversion: Translating the 8-bit binary number into a proportional voltage (e.g., $10000000_2$ results in $0\text{V}$).
* Sample and Hold (PAM): Maintaining the voltage until the next frame arrives, creating a Pulse Amplitude Modulation signal.
* Reconstruction: Passing the "staircase" PAM signal through a low-pass filter to recover the smooth original message.

#### Synchronization Requirements
The TIMS PCM Decoder is not self-clocking and requires external timing to function correctly:
* Clock Synchronization: The decoder must use the exact same clock as the encoder (often "stolen" via a direct cable) to prevent reading bits twice or missing them entirely.
* Frame Synchronization (FS): An external FS signal is required to identify the beginning of each frame. Without this, the bits are misaligned, and the output voltage will be incorrectly interpreted.

### Encoding & Decoding Process
The transition from analog to digital (and back) follows these core stages:
1. Sampling & Quantization: The analog signal ($-2\text{V}$ to $+2\text{V}$) is sampled. Each sample is rounded to the nearest of 256 quantization levels.
2. Serialization: The 8-bit binary value is transmitted bit-by-bit in frames, starting with the Most Significant Bit (MSB/bit-7).
3. Reconstruction: The decoder converts these bits back into a Pulse Amplitude Modulation (PAM) signal. A low-pass filter then smooths the "staircase" PAM signal to recover the original waveform.


### PCM Encoding & Decoding Experiment Equipment 
* Emona Telecom-Trainer 101 (plus power-pack)
* Dual Channel 20Mhz oscilloscope
* Two Emona Telecom-Trainer 101 oscilloscope leads
* Assorted Emona Telecom’s Trainer 101 patch leads
* One set of headphones (Sterio)

<details>
  <summary>RESULTS in PCM Encoding</summary>

  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/23952d2782739c11364ed5e8dcec5f8bd32646ba/Exp%2012/09fedce5-bed5-4c6e-834e-c720a440f826.jpg" alt="PCM Encode">

  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/23952d2782739c11364ed5e8dcec5f8bd32646ba/Exp%2012/56ff2cdf-a905-49cb-bce7-511ff8da2c75.jpg" alt="PCM Encode">
  <i>clock adjusted</i>

  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/23952d2782739c11364ed5e8dcec5f8bd32646ba/Exp%2012/31687015-c47c-4b59-ae3d-e85fc642d4b9.jpg" alt="PCM Encode">
  <i>synchronize</i>

  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/23952d2782739c11364ed5e8dcec5f8bd32646ba/Exp%2012/c94fda36-592a-4799-914a-5271649749cb.jpg" alt="PCM Encode">
  <i>adjusted time</i>

Complete Experiment 
[Output Continuation](https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/0067b2a9344d3019990ed403c6d92b585b566617/Exp%2012/Exp12.COMS2.pdf)

</details>

<details>
  <summary>RESULTS in PCM Decoding</summary>
 
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/06c5e80d948165ffa29717e1d77a026485766e11/Exp%2013/FIGURE%202.png" alt="PCM Decode">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/06c5e80d948165ffa29717e1d77a026485766e11/Exp%2013/FIGURE%203.png" alt="PCM Decode">

   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/06c5e80d948165ffa29717e1d77a026485766e11/Exp%2013/FIGURE%204.png" alt="PCM Decode">

   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/06c5e80d948165ffa29717e1d77a026485766e11/Exp%2013/fig%205.png" alt="PCM Decode">

   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/06c5e80d948165ffa29717e1d77a026485766e11/Exp%2013/fig%2010.png" alt="PCM Decode">

   </details>

   ## IV - Bandwidth Limiting and Restoring Digital Signals
   In the classical communications model, a transmitter sends a message to a receiver through a channel (such as copper wire, fiber optics, or airwaves). However, every channel acts as a natural filter with a specific bandwidth, leading to two primary      types of distortion:
   1. Amplitude Distortion (Attenuation)
      All channels attenuate frequencies outside their bandwidth. Since both analog (AM) and digital signals are composed of multiple sine waves (harmonics), a narrow bandwidth filters out these essential components. For digital signals, losing higher harmonics rounds off the edges of square waves, making it difficult for a receiver to distinguish between logic levels.
   2. Channels also shift the phase of different sine waves by varying amounts. Even if the amplitude is maintained, a phase shift (e.g., 180°) alters how these waves recombine, further warping the signal's shape.

   ### Consequences for Digital Systems
   In systems like Pulse Code Modulation (PCM), these distortions lead to "noisy" recovery. If the signal shape is too degraded, the decoder misinterprets the logic levels, resulting in bit errors and incorrect voltage generation.

   ### Experiment Equipment 
   * Emona Telecom-Trainer 101 (plus power-pack)
   * Dual Channel 20Mhz oscilloscope
   * Two Emona Telecom-Trainer 101 oscilloscope leads
   * Assorted Emona Telecom’s Trainer 101 patch leads
   * One set of headphones (Sterio)

   <details>
  <summary>RESULTS</summary>
    <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/c59acad71279a8863070bbad441eecbe52d09949/Exp%2014/14BPART1.png" alt="Limiting and restoring">

   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/c59acad71279a8863070bbad441eecbe52d09949/Exp%2014/14BPART2.png" alt="Limiting and restoring">

   </details>

   ## V - Summary 
   [Complete Experimental Questions and Answers]( https://github.com/EarlArugay/Telecommunications-Engineering-Modular-Analysis-of-Analog-FM-and-Digital-PCM-Architectures/blob/1106fcdf1f7cbfe0371ee50407b2318c254873f1/Data/Q%26A-Telecommunications-Engineering-Modular-Analysis-of-Analog-FM-and-Digital-PCM-Architectures-.pdf)

   ## VI - Learnings 
   






