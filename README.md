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

## FM Modulation & Demodulation 
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

#### FM Modulator & Demodulator Experiment equipment 
* Emona Telecom-Trainer 101 (plus power-pack)
* Dual Channel 20Mhz oscilloscope
* Two Emona Telecom-Trainer 101 oscilloscope leads
* Assorted Emona Telecom’s Trainer 101 patch leads
* One set of headphones (Sterio)


<details>
  <summary>RESULTS in FM Modulator</summary>

  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.1.jpg" alt="Modulator">
  
  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.2.jpg" alt="Modulator">
  
  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.3.jpg" alt="Modulator">
  
  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.4.jpg" alt="Modulator">
  
  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.5.jpg" alt="Modulator">
  
  <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.6.jpg" alt="Modulator">
  
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.7.jpg" alt="Modulator">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.8.jpg" alt="Modulator">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.9.jpg" alt="Modulator">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/f378e541965ba37451978bb614b893e90962fdc4/Exp%209/9.10.jpg" alt="Modulator">
   
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


## Sampling and Reconstruction 
While modern communication increasingly relies on digital transmission for its superior noise resistance, analog messages (such as speech) must first be converted via sampling. This process involves measuring the analog signal's voltage at regular intervals using a digital sampling signal.

### Sampling Methods
* Natural Sampling: The sampled signal follows the analog message's voltage for the duration of the sampling pulse.
* Sample-and-Hold (PAM): The voltage is fixed at the instant of measurement, creating a "flat-top" pulse. This is often required for systems that cannot process fluctuating signal levels during a single sample.

#### Mathematical Model and Recovery
Sampling is mathematically defined as the multiplication of the message signal by the sampling signal:

$$\text{Sampled Message} = (\text{DC} + \text{Fundamental} + \text{Harmonics}) \times \text{Message}$$

This multiplication creates a complex output consisting of the original message frequency, plus various sum and difference frequencies (sidebands) centered around the sampling frequency and its harmonics.

To recover the original message, the sampled signal is passed through a Low-Pass Filter (LPF). The filter rejects the high-frequency harmonics and sidebands, allowing only the original low-frequency message signal to pass through.
          
 #### Experiment Equipments 
 * Emona Telecom-Trainer 101 (plus power-pack)
 * Dual Channel 20Mhz oscilloscope
 * Two Emona Telecom-Trainer 101 oscilloscope leads
 *  Assorted Emona Telecom’s Trainer 101 patch leads
  
  <details>
  <summary>RESULTS</summary>

   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.1.jpg" alt="Sampling">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.2.jpg" alt="Sampling">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.3.jpg" alt="Sampling">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.4.jpg" alt="Sampling">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.5.jpg" alt="Sampling">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.6.jpg" alt="Sampling">
   
   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.7.jpg" alt="Sampling">

   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.8.jpg" alt="Sampling">

   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.9.jpg" alt="Sampling">

   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.10.jpg" alt="Sampling">

   <img src="https://github.com/Johnvy-M/COMMS-2-LAB.---System-Analysis-of-FM-Sampling-and-PCM-/blob/5b4df2d824e5ee28cc9dd43716f1d5e0767ec4ae/Exp%2011/11.11.jpg" alt="Sampling">

  </details>

   







