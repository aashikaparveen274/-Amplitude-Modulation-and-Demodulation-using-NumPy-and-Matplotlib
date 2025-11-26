# -Amplitude-Modulation-and-Demodulation-using-NumPy-and-Matplotlib

__Aim__: 

To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 

__Apparatus Required__: 

Software: Python with NumPy and Matplotlib libraries 
Hardware: Personal Computer 

__Theory__: 

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting 
information via a radio carrier wave. In AM, the amplitude of the carrier wave is varied in proportion to that of 
the message signal. The general form of an AM signal is: 


__Algorithm__:
1. Initialize Parameters: Set the values for carrier frequency, message frequency, and sampling frequency. 
2. Generate Time Axis: Create a time vector for the signal duration. 
3. Generate Message Signal: Define the message signal as a cosine wave. 
4. Generate Carrier Signal: Define the carrier signal as a cosine wave. 
5. Modulate Signal: Apply the AM formula to obtain the modulated signal. 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

__Program__:
```
import numpy as np

import matplotlib.pyplot as plt

Ac = 14.3 # Carrier amplitude

fc = 2200 # Carrier frequency in Hz

Am = 12.3# Message signal amplitude

fm = 220 # Message signal frequency in Hz

fs = 12000 # Sampling frequency

t = np.arange(0, 2/fm, 1/fs) # Time vector

Em = Am * np.sin(2 * np.pi * fm * t)

Ec = Ac * np.sin(2 * np.pi * fc * t)

Eam = (Ac + Am * np.sin(2 * np.pi * fm * t)) * np.sin(2 * np.pi * fc * t)

plt.figure(figsize=(10, 6))

plt.subplot(3, 1, 1)

plt.plot(t, Em)

plt.grid()

plt.subplot(3, 1, 2)

plt.plot(t, Ec)

plt.grid()

plt.subplot(3, 1, 3)

plt.plot(t, Eam)

plt.grid()

plt.tight_layout()

plt.show()
```
__Calculation__:

![WhatsApp Image 2025-11-26 at 20 12 30_91df2c98](https://github.com/user-attachments/assets/1f312f3e-3cd4-4c87-9ae0-d3d8f3a8accf)


__Tabulation__:

![WhatsApp Image 2025-11-26 at 20 06 50_acd65bd6](https://github.com/user-attachments/assets/702ca46f-d44a-4abb-9f0f-11f0420cc10e)



 __Output__:

 <img width="994" height="590" alt="image" src="https://github.com/user-attachments/assets/120d294a-6de1-402d-a133-0a5871e1ba27" />



 __Result__:

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. Thus, AM is implemented using numPy and Matplotlib. 

