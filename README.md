# Auto-correlation-and-PSD

# Aim
Write a program for Autocorrelation and Power Spectral Density (PSD) of signals in Scilab and verify the Wiener–Khinchin relation.

# Equipments Needed
Computer with Intel i3 processor (or higher)

Scilab software

# Theory
The Wiener–Khinchin theorem states that:

The Power Spectral Density (PSD) of a wide-sense stationary random process is the Fourier Transform of its autocorrelation function.

<img width="466" height="74" alt="image" src="https://github.com/user-attachments/assets/c92ed74a-0f9d-4924-945a-da1cdb61a763" />

This relationship bridges the time-domain correlation and frequency-domain power representations of a signal.

# Algorithm
Load or Define the Signal: Input your time-domain signal.

Compute Autocorrelation: Calculate the autocorrelation function of the signal.

Compute Power Spectral Density (PSD):

Estimate the PSD using either:

Fourier Transform of the autocorrelation function, or

Methods like Welch’s periodogram.

Plot Results: Visualize both the autocorrelation function and PSD.

Procedure

Refer to the algorithm and write the code for the experiment.

Open Scilab on your system.

Type your code in a new editor.

Save the file.

Execute the code.

If any errors occur, debug and re-run the program.

Verify the generated waveform using tabulation and model waveform comparison.

# Program (Scilab Code)

clc

clear all; 

t=0:0.01:2*%pi;

x = 2*sin(3*t) + 0.5*sin(10*t);

subplot(3,2,1); 

plot(x); 

au=xcorr(x,x);

subplot (3,2,2); 

plot (au); 

v=fft(au); 

subplot(3,2,3);

plot(abs(v)); 

fw=fft(x); 

subplot(3,2,4); 

plot(fw); 

fw2=(abs(fw)).^2;

subplot(3,2,5); 

plot(fw2);

# Output:

![WhatsApp Image 2025-11-27 at 11 00 41_e574bccb](https://github.com/user-attachments/assets/03a8257e-9965-4ce7-a7b1-b1a93e65f8cd)

![WhatsApp Image 2025-11-27 at 19 53 39_fd53ffc4](https://github.com/user-attachments/assets/6aba0df5-4df0-40e1-b4cb-65c5c04261a0)

# Result:
Thus the Autocorrelation and PSD are executed in Scilab and output is verified.
