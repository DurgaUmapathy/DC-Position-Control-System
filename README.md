# DC-Position-Control-System
## Aim:
To control the position of motor having the following specifications using MATLAB.<br>
(J) moment of inertia of the rotor = 3.2284E-6 kg.m^2<br>
(b) motor viscous friction constant = 3.5077E-6 N.m.s<br>
(Kt) motor torque constant = 0.0274 N.m/Amp<br>
(R) electric resistance = 4 Ohm<br>
(L) electric inductance = 2.75E-6H<br>
## Apparatus Required:
Computer with MATLAB software
## Theory: 
<img width="1600" height="1320" alt="WhatsApp Image 2026-11-06 at 9 08 28 AM" src="https://github.com/user-attachments/assets/0a8181d7-dcc2-436d-a5a3-01f5408d987c" />
<img width="1016" height="1599" alt="WhatsApp Image 2026-11-06 at 9 09 13 AM" src="https://github.com/user-attachments/assets/53b28e67-623a-4eb3-8923-8ccac72ed8ad" />


## Procedure:
1.	Open MATLAB software
2.	Open a new script file.
3.	Type the program.
4.	Save and Execute the program.
5.	Analyse the output in open loop and closed loop.

## Program
J=3.2284e-6
B=3.5077e-6
kt=0.0274
Rf=4
Lf=2.75e-6
num=[kt]
den=[Lf*J Rf*J+B*Lf Rf*B 0]
ol_sys=tf(num,den)
subplot(1,2,1)
   step(ol_sys)
cl_sys=feedback(ol_sys,1)
subplot(1,2,2)
   step(cl_sys)
## Output
<img width="557" height="504" alt="csexp2" src="https://github.com/user-attachments/assets/e50963b4-43cf-4b36-8507-066761dbd95d" />

## Result
Thus, the position of dc motor is controlled using MATLAB. 
