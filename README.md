# DSP
1 
1. Unit step:
n = input(“enter the value”)
t = 0 : n-1
y = ones(1,n)
stem(t,y)
title(“plot of unit step signal”)
xlabel(“number of samples”)
ylabel(“amplitude”)
grid on
2. Ramp signal
n = input(“enter the value”)
t = 0 : n-1
stem(t,t)
title(“plot of ramp signal”)
xlabel(“number of samples”)
ylabel(“amplitude”)
grid on
3. Impulse signal
t = -2 : 2
y = [zeros(1,2),ones(1,1),zeros(1,2)]
stem(t,y)
title(“plot of impulse signal”)
xlabel(“number of samples”)
ylabel(“amplitude”)
grid on
4. Sine wave
t = 0 : 0.01 : 5
y = sin(2*pi*t)
plot(t,y)
title(“plot of sine wave”)
xlabel(“time”)
ylabel(“amplitude”)
grid on

2
PROGRAM FOR LINEAR CONVOLUTION:
x = input("enter the first sequence");
subplot(3,1,1);
stem(x);
xlabel("number of samples");
ylabel("amplitude");
title("first sequence");
y = input("enter the second sequence");
subplot(3,1,2);
stem(y);
xlabel("number of samples");
ylabel("amplitude");
title("second sequence");
z = conv(x,y);
subplot(3,1,3);
stem(z);
xlabel("number of samples");
ylabel("amplitude");
title("linear convolution");
grid on;
disp("the resultant signal is z =");
disp(z)

PROGRAM FOR CIRCULAR CONVOLUTION:
x = input("enter the first sequence");
subplot(3,1,1);
stem(x);
xlabel("number of samples");
ylabel("amplitude");
title("first sequence");
y = input("enter the second sequence");
subplot(3,1,2);
stem(y);
xlabel("number of samples");
ylabel("amplitude");
title("second sequence");
l1 = length(x);
l2 = length(y);
N = max(l1,l2);
z = cconv(x,y,N);
subplot(3,1,3);
stem(z);
xlabel("number of samples");
ylabel("amplitude");
title("circular convolution");
grid on;
disp("the resultant signal is z =");
disp(z)

3
clear all;
close all;
t=-100:01:100;
fm=0.02;
x=cos(2*pi*t*fm);
subplot(2,2,1);
plot(t,x);
xlabel('time in sec');
ylabel('x(t)');
title('continuous time signal');
fs1=0.02;
n1=-2:2;
x1=cos(2*pi*fm*n1/fs1);
subplot(2,2,2);
stem(n1,x1);
title('discrete time signal x(n) with fs<2fm');
xlabel('n');
ylabel('x(n)');
fs2=0.04;
n2=-4:4;
x2=cos(2*pi*fm*n2/fs2);
subplot(2,2,3);
stem(n2,x2);
title('discrete time signal x(n) with fs=2fm');
xlabel('n');
ylabel('x(n)');
n3=-50:50;
fs3=0.5;
x3=cos(2*pi*fm*n3/fs3);
subplot(2,2,4);
DIGITAL SIGNAL PROCESSING
ECE DEPARTMENT, MIT SOES, MIT ADT UNIVERSITY, PUNE 3
stem(n3,x3);
xlabel('n');
ylabel('x(n)');
title('discrete time signal x(n) with fs>2fm');
disp(x);
disp(x1);
disp(x2);
disp(x3);

4
1. For x = 2^n - 3^n
syms n;
x = 2^n - 3^n;
y = ztrans(x);
disp(y);
m = iztrans(y)
2.For x = sin(n)
syms n;
x = sin(n);
y = ztrans(x);
disp(y);m = iztrans(y)
3.For x = delta(n)
syms n;
x = kroneckerDelta(n, 0);
y = ztrans(x);
disp(y);
m = iztrans(y)
4.For x = cos(n)
syms n;
x = cos(n);
y = ztrans(x);
disp(y);
m = iztrans(y)
5.For x = exp(5n)
syms n;
x = exp(5*n);
y = ztrans(x);
disp(y);
m = iztrans(y)
6.For x = sinc(n)syms n;
x = sinc(n);
y = ztrans(x);
disp(y);
m = iztrans(y)
7.For x = heaviside(n)
syms n;
x = heaviside(n);
y = ztrans(x);
disp(y);
m = iztrans(y)
8.For x = 5^n - cos(n) + exp(-7*n) - 8*n
syms n;
x = 5^n - cos(n) + exp(-7*n) - 8*n
y = ztrans(x);
disp(y);
pretty(y);
m = iztrans(y)
