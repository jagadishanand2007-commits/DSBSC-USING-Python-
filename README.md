# DSBSC-USING-Python-
## Aim

To implement and analyze  (DSBSC) using Python's NumPy and Matplotlib libraries.

## Apparatus Required

1.Software: Python with NumPy and Matplotlib libraries

2.Hardware: Personal Computer
## Theory

DSB-SC (Double Sideband Suppressed Carrier) is a type of amplitude modulation where the carrier wave is suppressed, and only the two sidebands (which contain the actual information) are transmitted. This saves power and reduces bandwidth waste compared to standard AM.

In DSB-SC, the amplitude of the carrier is still varied according to the message signal, but the carrier itself is not transmitted.

## Algorithm

1.Initialize Parameters: Set the values for carrier frequency, message frequency and  sampling frequency.

2.Generate Time Axis: Create a time vector for the signal duration.

3.Generate Message Signal: Define the message signal as a cosine wave.

4.Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.

5.Generate AM Signal: Apply the DSBSC modulation formula to obtain the modulated signal.

6.Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## Program
~~~
import numpy as np
import matplotlib.pyplot as plt
Am=7.1
Fm=559
Ac=14.2
Fs=55900
Fc=5590

t=np.arange(0,2/Fm,1/Fs)

m=Am*np.cos(2*np.pi*Fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*np.pi*Fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s1 = (Ac + m) * np.cos(2 * np.pi * Fc * t)
s2=(Ac-m)*np.cos(2*np.pi*Fc*t)
s=s1-s2
plt.subplot(3,1,3)
plt.plot(t,s)
~~~
## Output Waveform

<img width="928" height="566" alt="image" src="https://github.com/user-attachments/assets/03fe4cd6-db96-4625-bbeb-1d94800ceb68" />


## Tabular Column
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/11e07fbf-d465-4e6b-9448-ae6d793628d5" />




## Result

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
