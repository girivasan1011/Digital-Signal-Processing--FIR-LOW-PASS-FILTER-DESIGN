# Digital-Signal-Processing--FIR-LOW-PASS-FILTER-DESIGN
## AIM:
To generate design of low pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Low Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
wc=input('enter the value of cut off frequency'); 
N=input('enter the value of filter'); 
alpha=(N-1)/2; 
eps=0.001; 
%High Pass Filter Coefficient
n=0:1:N-1; 
hd=(sin(pi*(n-alpha+eps))-sin((n-alpha+eps)*wc))./(pi*(n-alpha+eps))
%Bartlett Window Sequence 
n=0:1:N-1; 
wh = 1 - (2 * abs(n - alpha) / (N - 1));
hn=hd.*wh
% Plot the High Pass Filter with Bartlett Window Technique
w=0:0.01:pi; 
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```

## OUTPUT:
<img width="692" height="618" alt="Screenshot 2025-11-06 112803" src="https://github.com/user-attachments/assets/41453f97-ce8d-45c7-ac23-9cdf7f15eb49" />

## RESULT:
![WhatsApp Image 2025-11-23 at 5 30 59 PM](https://github.com/user-attachments/assets/a07cf4dc-5221-43e3-8dc2-2d325f7bb441)

