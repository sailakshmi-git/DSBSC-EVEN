# DSBSC-EVEN
EX NO: 2 DSB-SC-AM MODULATOR AND DEMODULATOR

AIM:

To write a program to perform DSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

EQUIPMENTS REQUIRED

• Computer with i3 Processor • SCI LAB

Note: Keep all the switch faults in off position

Algorithm:

Define Parameters: • Fs: Sampling frequency. • T: Duration of the signal. • Fc: Carrier frequency. • Fm: Frequency of the message signal. • Amplitude: Maximum amplitude of the message signal.
Generate Signals: • Message Signal: A sinusoidal signal that will be modulated. • Carrier Signal: A high-frequency sinusoidal signal used for modulation.
DSBSC Modulation: • Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
DSBSC Demodulation: • Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components). • Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
Visualization: Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation. PROCEDURE
• Refer Algorithms and write code for the experiment. • Open SCILAB in System • Type your code in New Editor • Save the file

• Execute the code • If any Error, correct it in code and execute again • Verify the generated waveform using Tabulation and Model Waveform

Model Waveform
<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/736bef01-c500-4225-85e4-92c4e2fdf692" />

Program

```
clc;
clear;
close;

// Parameters
Am = 3.7;        // Message amplitude
Ac = 7.4;        // Carrier amplitude
fm = 166;      // Message frequency (Hz)
fc = 1660;     // Carrier frequency (Hz)
fs = 16600;    // Sampling frequency (Hz)

// Time vector
t = 0:1/fs:0.05;

// Message signal
m = Am * sin(2*%pi*fm*t);

// Carrier signal
c = Ac * sin(2*%pi*fc*t);

// DSB-SC modulation
dsb_sc = m .* c;

// Plotting
subplot(3,1,1)
plot(t, m)
title("Message Signal")
xlabel("Time")
ylabel("Amplitude")

subplot(3,1,2)
plot(t, c)
title("Carrier Signal")
xlabel("Time")
ylabel("Amplitude")

subplot(3,1,3)
plot(t, dsb_sc)
title("DSB-SC Modulated Signal")
xlabel("Time")
ylabel("Amplitude")

```


Output Graph:

```
![WhatsApp Image 2026-03-20 at 9 08 06 AM](https://github.com/user-attachments/assets/b6f78059-8486-4d00-9594-b404ce65f37d)
```

Tablular Column:

```
<img width="772" height="640" alt="image" src="https://github.com/user-attachments/assets/b205472a-b5e9-430c-ab10-f25cdd0046f6" />
```

Result

Thus the DSB-SC-AM Modulation and Demodulation is generated.
