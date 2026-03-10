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

### Demodulation Methods
There are numerous ways to recover the original message from an FM signal, including:
* Slope detectors and Ratio detectors.
* Phase-locked loops (PLL).
* Zero-crossing detectors (the primary method used for introductory experiments).

### The Zero-Crossing Detector (ZCD)
The Zero-crossing Detector is an efficient method for FM demodulation. It operates by converting frequency variations into a measurable DC component.

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
          
  







