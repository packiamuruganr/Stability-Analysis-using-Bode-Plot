# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![519801215-1539b4b2-f106-47fe-9344-a525aee2366c](https://github.com/user-attachments/assets/6ec61719-8485-424e-aac0-3d94d8359bcc)
![519801460-aa2daa3e-5597-453e-af33-1ad0e090315b](https://github.com/user-attachments/assets/482515d5-e8d6-4cd2-8ace-7033ef8c43bd)
![519801601-014313a9-b53e-44d4-8620-b81f1346f242](https://github.com/user-attachments/assets/6b5f8d14-3abd-4efa-9fda-bc4e07cf55c2)

## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
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
```

## Output:
<img width="707" height="630" alt="514058307-c43c55ab-6b64-4424-827f-8ff179b29b97" src="https://github.com/user-attachments/assets/ec69d7f4-231f-4932-8926-e3b1eb763cbd" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12 <br>
Phase Margin = 60 <br>
Gain crossover frequency = 0.907 <br>
Phase crossover frequency = 4.4721 <br>
The system is stable.
