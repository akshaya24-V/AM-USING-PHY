# AM-USING-PHY
# AIM:
To implement and analyze Amplitude modulation (AM) using Python's NumPy and Matplotlib libraries.

# EQUIPMENTS REQUIRED
• Software: Python with NumPy and Matplotlib libraries Hardware: Personal Computer

# THEORY:
Theory of Amplitude Modulation (AM) AM is an analog modulation technique where the amplitude of a high-frequency carrier wave is varied in proportion to the instantaneous amplitude of a low-frequency message signal (or baseband signal).

# PROCEDURE
1.Install/Import Libraries: Ensure the necessary libraries, NumPy (np) for numerical calculation and Matplotlib (plt) for plotting, are imported. This is done by the first two lines of the code.

2.Define Parameters: Define the amplitudes (Am, Ac) and frequencies (Fm, Fc, Fs) for the message and carrier signals. These constants determine the characteristics of the generated signals.

3.Create Time Base: Generate a time vector (t) using np.arange(). This array represents the discrete time points over which the signals will be sampled and calculated.

4.Generate Signals: Use the defined parameters and the time base (t) to calculate the three required signal arrays: the message signal (m), the carrier signal (c), and the final AM signal (s).

5.Plot and Visualize: Use the plt.subplot() function to create a figure with three separate axes and plot the three generated signals (m, c, and s) in their respective positions for visual comparison. Finally, use plt.show() to display the generated graph.

# Program:

import numpy as np

import matplotlib.pyplot as plt
Am = 3.3

Fm = 290

Ac = 6.6

Fc = 2900

Fs = 29000

t = np.arange(0, 2 / Fm, 1 / Fs)

m = Am * np.cos(2 * np.pi * Fm * t)

c = Ac * np.cos(2 * np.pi * Fc * t)

s = (Ac + m) * np.cos(2 * np.pi * Fc * t)

plt.figure(figsize=(10, 8))

plt.subplot(3, 1, 1)

plt.plot(t, m)

plt.subplot(3, 1, 2)

plt.plot(t, c)

plt.subplot(3, 1, 3)
plt.plot(t, s)

plt.tight_layout()

plt.show()

# Output Waveform

<img width="713" height="586" alt="image" src="https://github.com/user-attachments/assets/702b1a42-fd19-490f-818d-0cea1f8c9343" />


# Tabulation
<img width="1279" height="655" alt="image" src="https://github.com/user-attachments/assets/e2836432-98fb-4fad-a28e-88eed84f6b3a" />


# RESULT:
Thus, the AMPLITUDE modulation using python is successfully done and the output is experimentally verified.
