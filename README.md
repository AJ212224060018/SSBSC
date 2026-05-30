# EXP NO: 3 SSB-SC-AM MODULATION using SCILAB

### Aim:

To write a program to perform SSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

### Equiptments Required:

• Computer

• SCI LAB
Note: Keep all the switch faults in off position

### Algorithm:

#### Define Parameters: 
  • Fs: Sampling frequency.
  
  • T: Duration of the signal.
  
  • Fc: Carrier frequency. 
  
  • Fm: Frequency of the message signal.
  
  • Amplitude: Maximum amplitude of the message signal.
  
#### Generate Signals: 
  • Message Signal: The baseband signal that will be modulated.
  
  • Carrier Signal: A high-frequency signal used for modulation.
  
  • Analytic Signal: Constructed using the Hilbert transform to get the in-phase and quadrature components.
  
#### SSBSC Modulation: 
  • Modulated Signal: Create the SSBSC signal using the in-phase and quadrature components, modulated by the carrier.
  
#### SSBSC Demodulation: 
  • Mixing: Multiply the SSBSC signal with the carrier to retrieve the message signal.
  
  • Low-pass Filtering: Apply a low-pass filter to remove high-frequency components and recover the original message signal.
#### Visualization:
  • Plot the message signal, carrier signal, SSBSC modulated signal, and the recovered signal after demodulation.
### Procedure:

  • Refer Algorithms and write code for the experiment. 
  
  • Open SCILAB in System 
  
  • Type your code in New Editor
  
  • Save the file

  • Execute the code 
  
  • If any Error, correct it in code and execute again 
  
  • Verify the generated waveform using Tabulation and Model Waveform

### Model Waveform:

<img width="598" height="271" alt="image" src="https://github.com/user-attachments/assets/351e261f-6bcc-4a72-a7ab-d6219ed88fe0" />

### Program:
~~~
Am=9.59;
fm=916;
Ac=15.344;
fc=9160;
fs=91600;
t=0:1/fs:2/fm;
em1=Am*cos(2*3.14*fm*t);
ec1=Ac*cos(2*3.14*fc*t);
em2=Am*sin(2*3.14*fm*t);
ec2=Ac*sin(2*3.14*fc*t);
edsbsc1=em1.*ec1;
subplot(4,1,1);
plot(t,em1);
edsbsc2=em2.*ec2;
subplot(4,1,2);
plot(t,ec1);
elsb=edsbsc1+edsbsc2;
subplot(4,1,3);
plot(t,elsb);
eusb=edsbsc1-edsbsc2;
subplot(4,1,4);
plot(t,eusb);
~~~
### Output Waveform:

<img width="758" height="720" alt="image" src="https://github.com/user-attachments/assets/695cd898-7a8c-4c48-b271-7628b544b456" />

### Tabulation:

### Result:
Thus, the SSB-SC-AM Modulation and Demodulation is experimentally done and the output is verified.
#
