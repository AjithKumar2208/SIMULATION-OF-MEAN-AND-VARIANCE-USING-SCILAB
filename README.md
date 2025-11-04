# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB

---
Aim:

To write a program for mean, variance and cross correlation in SCILAB and verify the output.

---
Apparatus Required


1.	Computer with i3 Processor
2.	SCI LAB

  ---
  
Theory

Mean and variance are two fundamental statistical parameters used to describe the characteristics of a dataset or signal. In Scilab, these parameters can be computed and simulated to analyze the behavior and spread of data, especially in signal and system analysis.

---

Algorithm

1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation 


---

Program
~~~
function X=f(x)
   z=10*(4-x)^2;
   X=x*z
endfunction
a=0;
b=1;
EX=intg(a,b,f);
function Y=c(y)
  z=10*(4-y)^2;
  Y=y*z;
endfunction
EY=intg(a,b,c); 
disp(EX,"i)Mean of X =");
disp(EY,"Mean of Y =");

function X=g(x)
    z=10*(4-x)^2;  
    X=x^2*z
endfunction
a=0;
b=1;
EX2=intg(a,b,g);
function Y=h(y)
    z=10*(4-y)^2;
    Y=y^2*z;
endfunction
EY2=intg(a,b,h);
vX2=EX2-(EX)^2;
vY2=EY2-(EY)^2;
disp(vX2,"ii)Variance of X");
disp(vY2," Variance of Y");

x= input("type in the reference sequence=");
y= input("type in the second sequence="); n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);

~~~

---

Output :

<img width="466" height="315" alt="image" src="https://github.com/user-attachments/assets/0899d8d4-893c-4ac1-8c8b-8237b0dba7c6" />


<img width="1728" height="936" alt="image" src="https://github.com/user-attachments/assets/aa5f5169-729d-4c84-aa14-51ccf505b668" />


---

Calculation:

![WhatsApp Image 2025-11-04 at 21 43 57_73ce2515](https://github.com/user-attachments/assets/3718e3cf-b2c5-499f-9d1e-ceb4ad32fd5a)


![WhatsApp Image 2025-11-04 at 21 43 58_42d86bb7](https://github.com/user-attachments/assets/22c7ff1c-24d3-444c-b3a1-f4e035ac2464)


![WhatsApp Image 2025-11-04 at 21 43 59_840a16cd](https://github.com/user-attachments/assets/92bff9cb-6a22-4f6f-8c11-999b2e44cb91)


![WhatsApp Image 2025-11-04 at 21 43 59_a7596dd6](https://github.com/user-attachments/assets/99e8ab81-dd5a-470b-b050-5b7325b047c0)


---

Result

The mean and variance of the given data or signal are successfully calculated and displayed using Scilab. The simulation shows that the mean represents the average or central value of the dataset, while the variance indicates the degree of spread of the data around the mean. These results help in understanding the statistical characteristics and variability of the simulated signal or random data.
