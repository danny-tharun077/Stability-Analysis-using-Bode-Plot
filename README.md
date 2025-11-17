# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![WhatsApp Image 2025-11-17 at 18 03 17_798dda1f](https://github.com/user-attachments/assets/154ade04-08e4-4772-9778-9131200f6550)

![WhatsApp Image 2025-11-17 at 18 03 18_e5272145](https://github.com/user-attachments/assets/d465c407-27da-4af3-a649-a125b2443d99)


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
<img width="1788" height="953" alt="image" src="https://github.com/user-attachments/assets/0c3fe222-c6be-45f4-81c2-d86cc68a21eb" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>

Gain margin = 12

Phase Margin = 60.42

Gain crossover frequency = 0.90 rad/s

Phase crossover frequency = 4.47 rad/s

The system is STABLE
