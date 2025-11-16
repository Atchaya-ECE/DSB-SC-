# DSBSC

# EX NO: 2	DSB-SC-AM MODULATOR AND DEMODULATOR

# AIM:

To write a program to perform DSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

# EQUIPMENTS REQUIRED
•	Computer with i3 Processor
•	SCI LAB

Note: Keep all the switch faults in off position

# Algorithm:

1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: A sinusoidal signal that will be modulated.
•	Carrier Signal: A high-frequency sinusoidal signal used for modulation.
3.	DSBSC Modulation:
•	Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
4.	DSBSC Demodulation:
•	Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components).
•	Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
5.	Visualization:
Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation.

# PROCEDURE
•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

# Model Waveform

<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/e7c7c7f8-ccf2-41ac-b1f3-325989941a6f" />

# Program
```
Ac=23.2;
Am=11.6;
fc=11600;
fm=1160;
fs=50000;
t=0:1/fs:2/fm;
Wm=2*3.14*fm;
Wc=2*3.14*fc;
Em=Am*sin(2*3.14*fm*t);
subplot(3,1,1);
plot(t,Em);
xlabel("Time(s)");
ylabel("Amplitude");
title("Message Signal m(t)");
Ec=Ac*sin(2*3.14*fc*t);
subplot(3,1,2);
plot(t,Ec);
xlabel("Time(s)");
ylabel("Amplitude");
title("Carrier Signal c(t)");
Edsbsc=((Am/2)*cos((Wc-Wm)*t))-((Am/2)*cos((Wc+Wm)*t));
subplot(3,1,3);
plot(t,Edsbsc);
xlabel("Time(s)");
ylabel("Amplitude");
title("DSB-SC Modulated Signal"); 
```

# Output Graph
![WhatsApp Image 2025-11-04 at 18 35 14_250955a1](https://github.com/user-attachments/assets/099509bb-47fe-4850-ae2e-56787427e24e)

# Tablular Column
![WhatsApp Image 2025-11-04 at 20 46 17_ef8a6b18](https://github.com/user-attachments/assets/25d52a9d-934b-4606-bb02-fc758cf7acf7)

# Calculation
![WhatsApp Image 2025-11-04 at 20 46 38_a6df924c](https://github.com/user-attachments/assets/88139955-fdfe-42c5-b5d6-dbe23b810adc)

# Result
![WhatsApp Image 2025-11-16 at 21 22 24_6dcc763d](https://github.com/user-attachments/assets/cdc9891f-9252-4ca4-a15b-341e4b22602a)


