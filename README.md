![image](https://github.com/himani2853/Audio_amplifier/assets/117065953/5ead83b2-4861-4e9f-bc52-a40f3bbe4973)![image](https://github.com/himani2853/Audio_amplifier/assets/117065953/ad315118-fd5f-49c3-9ae6-93fa3676ca0d)# Audio_amplifier
An Audio Amplifier is an analog circuit that takes a small audio signal as input and increases its amplitude without changing its quality or waveform. It is usually used to amplify signal obtained from a microphone by boosting its power to a level required to be playable by a speaker.

It is constructed using 4 stages:
1) Pre-Amplifier -> An input from the microphone cannot be directly sent to the power amplifier as this would result in an extremely noisy signal that is incapable of driving the load (speaker). Hence, we use a pre-amp to amplify a quiet mic-level signal up to a louder line–level signal which is standard for transmitting analog signal b/w equipment. Here the pre-amp is supposed to have a high impedance (so that even a very small amount of current can be sensed) and a low output impedance (to make sure there is no voltage drop at the output).
We have implemented a pre-amplifier using DIFFERENTIAL AMPLIFIER in the single-ended unbalanced output configuration.

2) Gain -> We are using a multi-stage cascade system for amplification for the following reasons:
Increasing the gain while maintaining the stability of the amplifier
To achieve better noise immunization
Here we are using a CE Amplifier to meet the below-mentioned requirements:
	1) High input impedance to avoid loading problems and to avoid the passage of input 
	current through it so that input signal is available for amplification
	2) High Voltage gain
	3) Low Current gain
	4) Low Output impedance

3) Filter -> We need to filter out high-frequency noise and tune our signal according to our requirements. We need a frequency range of 50 Hz – 20 kHz for our circuit.
Here we are using a low pass filter to eliminate frequencies above 20kHz 
 A high-pass for 50Hz hasn’t been used since there is negligible attenuation in the range of 0 to 50Hz.
Our Low pass filter is a passive filter made using a resistor and a capacitor having a cutoff frequency of 20 kHz.
This is followed by a unity gain non-inverting buffer made using Op-Amp to act as a buffer between the filter and power amplifier. This is done to prevent any loading. 



4) Power-Amplifier -> Power Amplifier is an electronic amplifier designed to increase the magnitude of power of a given input signal. 
The power of the input signal is increased to a level high enough to drive loads of output device, here speaker. It is the final block of this amplifier chain to drive the speaker directly. 
The input signal to a power amplifier needs to be above a certain threshold. So, instead of directly feeding the input from the mic to the power amplifier, it is first pre-amplified using a differential amplifier and CE amplifier and is sent as input to the power amplifier. 





