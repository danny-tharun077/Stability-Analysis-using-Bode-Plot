# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:



## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
~~~
num=1
den=[0.05 0.6 1 0]
sys=tf(num,den)
bode(sys)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
~~~

## Output:
<img width="1654" height="1024" alt="image" src="https://github.com/user-attachments/assets/e3067cb2-6ee3-4ce8-a43b-b6792fe5fa6f" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 

Phase Margin = 

Gain crossover frequency = 0.902 rad/s

Phase crossover frequency = 4.43 rad/s

The system is STABLE
