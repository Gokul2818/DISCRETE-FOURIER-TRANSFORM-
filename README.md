# EXP 1 A : COMPUTATION OF DFT USING DIRECT AND FFT

# AIM: 

# To Obtain DFT and FFT of a given sequence in SCILAB. 

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
// DISCRETE FOURIER TRANSFORM 
```
clc; 
clear; 
xn=[1 2 3 4 4 3 2 1]; 
 
n1=0:1:length(xn)-1; 
subplot(3,1,1); 
plot2d3(n1,xn); 
xlabel('Time n'); 
ylabel('Amplitude xn'); 
title('Input Sequence'); 
j=sqrt(-1); 
N=length(xn); 
Xk=zeros(1,N); 
for k=0:N-1 
for n=0:N-1 
Xk(k+1)=Xk(k+1)+xn(n+1)exp((-j*2%pi*k*n)/N); 
end   
end 
disp(Xk) 
K1=0:1:length(Xk)-1; 
magnitude=abs(Xk) 
subplot(3,1,2); 
plot2d3(K1,magnitude); 
xlabel('frequency(Hz)'); 
ylabel('magnitude(gain)'); 
title('magnitude spectrum'); 
angle = atan(imag(Xk),real(Xk)) 
subplot(3,1,3); 
plot2d3(K1,angle); 
xlabel('frequency(Hz)'); 
ylabel('Phase'); 
title('Phase spectrum');
```
# OUTPUT:

![WhatsApp Image 2025-11-21 at 00 05 38_f87bf558](https://github.com/user-attachments/assets/b02c0bf9-4e22-494a-a319-b69446a4c6e0)

# RESULT: 

Thus, the Discrete fourier transform of the given sequence were obtained and its magnitude and phase spectrum were plotted.
